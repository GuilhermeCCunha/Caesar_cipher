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

### Algorithm solution 2

## Demonstration

## Show your support

Please ⭐️ this repository if you liked it!

## Author

- GitHub: [@GuilhermeCCunha](https://github.com/GuilhermeCCunha)
