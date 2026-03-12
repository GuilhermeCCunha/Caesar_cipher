# Caesar Cipher

<img width="406" height="375" alt="caesar_cipher_disk" src="https://github.com/user-attachments/assets/26b14417-b223-4e7a-b15d-06d95b5f71ec" />

<br/> <br/>
Caesar Cipher in Ruby

## Getting Started

Clone or download zip file:

```bash
git clone https://github.com/GuilhermeCCunha/Caesar_cipher.git
```

You need to have Ruby installed on your Linux system.

### Creating Custom Commands

Put the command below into your .bashrc

```bash
# User specific environment
if ! [[ "$PATH" =~ "$HOME/.local/bin:$HOME/bin:" ]]; then
    PATH="$HOME/.local/bin:$HOME/bin:$PATH"
fi
export PATH
```

Enter the directory (folder) you've just cloned.

```bash
cd Caesar_cipher
```

Type the following command to create bin directory in your home directory.

```bash
mkdir $HOME/bin
# or
mkdir -p $HOME/.local/bin
```
Type the following command to copy files to the new directory.

```bash
cp ccipher* $HOME/bin
# or 
cp ccipher* $HOME/.local/bin
```

## Solutions

### Algorithm solution 1

The simple solution to this is to indicate to the numbers over 26 to wrap around and start over again with an index of 1, and not 25.
The simple way to do this is to use the modulo (%).

See the `ccipher` file for more details.

### Algorithm solution 2

Array#rotate: Eliminates the need for the modulo (%) when shifting alphabet arrays. <br>
String#tr: Handles substitution efficiently, including non-alphabetic characters (they are ignored).

See the `cciphertr` file for more details.

## Demonstration

### Hello World

#### Encoding

![caesar_cipher_hello_encoding](https://github.com/user-attachments/assets/d01eefb2-5769-4ad2-8c0c-6959f911bea2)

#### Decoding

![caesar_cipher_hello_decoding](https://github.com/user-attachments/assets/15482899-72c9-4f2b-84f6-8886169aa3d4)

### The default shift value is 1

![caesar_cipher_default_shift_value](https://github.com/user-attachments/assets/1b482944-50b6-4161-a96f-f5ffc26d4eb4)

## Working with Files

### Command Substitution

Encoding a file.

```bash
ccipher "$(cat loremipsum.txt)" 3
```

Encoding a file and creating a new one.

```bash
ccipher "$(cat loremipsum.txt)" 3 > loremipsum-encoded.txt
```


## Show your support

Please ⭐️ this repository if you liked it!

## Author

- GitHub: [@GuilhermeCCunha](https://github.com/GuilhermeCCunha)
