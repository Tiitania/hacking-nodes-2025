#### Description

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).

#### Hints 
- Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
- [println!](https://doc.rust-lang.org/std/macro.println.html)
- Rust has some pretty great compiler error messages. Read them maybe?

## Solución
-Tener una extensión para ver las cookies
-Ingersamos cualquier usuario y contraseña
-Copiamos la cookie que nos salga y lo decodificamos de base 64

```
descromprimimos el archivo y buscamos nuestro codigo rust, con ello ya solo corregimos los errores que en este caso es el prinln
lo compilamos y obtenemos nuestra bandera

codigo corregido:
use xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    let key = String::from("CSUCKS"); // La sentencia termina con punto y coma

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "7f", "5a", "60", "50", "11", "38", "1f", "3a", "60", "e9", "62", "20", "0c", "e6", "50", "d3", "35"];

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decryption object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // Se sale de la función main si hay error
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!("{}", String::from_utf8_lossy(&decrypted_buffer)); // Imprimir la cadena descifrada
}


picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```

https://gchq.github.io/CyberChef/
