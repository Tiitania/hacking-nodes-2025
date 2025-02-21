## Binary Search
### Description 
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

Additional details will be available after launching your challenge instance.

### Hint

- Have you ever played hot or cold? Binary search is a bit like that.
- You have a very limited number of guesses. Try larger jumps between numbers!
- he program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solución 
tratar de acertar el numero correcto con el lower y higher
```
Connection to atlas.picoctf.net closed.
Gurihacker-picoctf@webshell:~$ ssh -p 50162 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 726
Lower! Try again.
Enter your guess: 725
Lower! Try again.
Enter your guess: 609
Higher! Try again.
Enter your guess: 650
Lower! Try again.
Enter your guess: 610
Higher! Try again.
Enter your guess: 620
Higher! Try again.
Enter your guess: 630
Congratulations! You guessed the correct number: 630
Here's your flag: picoCTF{g00d_gu355_3af33d18}

```

