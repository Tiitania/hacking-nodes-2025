#### Description
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz).

#### Hints 
- Read the comments...darn it!



```
los comentarios del codigo nos quita el unsafe, por lo que lo borramos y funcionaria nuestro codigo

use xor_cryptor::XORCryptor;

fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &mut String) {
    // Key for decryption
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decryption object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return;
    }
    let xrc = res.unwrap();

    // Did you know you have to do "unsafe operations in Rust?
    // https://doc.rust-lang.org/book/ch19-01-unsafe-rust.html
    // Even though we have these memory safe languages, sometimes we need to do things outside of the rules
    // This is where unsafe rust comes in, something that is important to know about in order to keep things in perspective

    -->>quitarlo // unsafe {
        // Decrypt the flag operations
        let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);

        // Creating a pointer
        let decrypted_ptr = decrypted_buffer.as_ptr();
        let decrypted_len = decrypted_buffer.len();

        // Unsafe operation: calling an unsafe function that dereferences a raw pointer
        let decrypted_slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);

        borrowed_string.push_str(&String::from_utf8_lossy(decrypted_slice));
   -->>quitarlo // }
    println!("{}", borrowed_string);
}

obtenemos lo sig al compilar:

picoCTF{n0w_y0uv3_f1x3d_1h3m_411}
```
