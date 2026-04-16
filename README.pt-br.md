# Caesar Cipher
🌏
[**English**][readme-en] |
Português

[![GitHub repo size][github-img]][github-url]
[![GitHub last commit][github-commit]][github-url]
[![Ruby][ruby]][ruby-lang]

<img width="406" height="375" alt="caesar_cipher_disk" src="https://github.com/user-attachments/assets/26b14417-b223-4e7a-b15d-06d95b5f71ec" />

<br/> <br/>
Caesar Cipher (Cifra de César) em Ruby

## Tabela de conteúdos

* [Começando](#começando)
  * [Criando Comandos Personalizados](#criando-comandos-personalizados)
* [Soluções](#soluções)
  * [Primeira solução do algoritmo](#primeira-solução-do-algoritmo)
  * [Segunda solução do algoritmo](#segunda-solução-do-algoritmo)
* [Demonstração](#demonstração)
  * [Olá Mundo](#olá-mundo)
    * [Codificação](#codificação)
    * [Decodificação](#decodificação)
  * [O valor padrão do deslocamento é 1](#o-valor-padrão-do-deslocamento-é-1)
* [Trabalhando com Arquivos](#trabalhando-com-arquivos)
  * [Substituição de Comando](#substituição-de-comando)
  * [XARGS](#xargs)
* [Mostre seu apoio](#mostre-seu-apoio)
* [Autor](#autor)

## Começando

Clone o repositório ou faça o download do arquivo zip:

```bash
git clone https://github.com/GuilhermeCCunha/Caesar_cipher.git
```

É necessário ter o Ruby instalado no seu sistema Linux.

<blockquote>
#!/usr/bin/env ruby
</blockquote>

Isso é chamado de **shebang**. Ele instrui o sistema a usar o interpretador Ruby para executar o script. O `env` localiza dinamicamente o interpretador Ruby com base no `PATH` do seu sistema.
Isso torna o script mais portátil.

### Criando Comandos Personalizados

Coloque o comando abaixo no seu arquivo .bashrc

```bash
# Ambiente específico do usuário
if ! [[ "$PATH" =~ "$HOME/.local/bin:$HOME/bin:" ]]; then
    PATH="$HOME/.local/bin:$HOME/bin:$PATH"
fi
export PATH
```

Acesse o diretório (pasta) que você acabou de clonar.

```bash
cd Caesar_cipher
```

Digite o seguinte comando para criar o diretório bin no seu diretório home.

```bash
mkdir $HOME/bin
# ou
mkdir -p $HOME/.local/bin
```

Digite o seguinte comando para copiar os arquivos para o novo diretório.

```bash
cp ccipher* $HOME/bin
# ou 
cp ccipher* $HOME/.local/bin
```

## Soluções

### Primeira solução do algoritmo

A solução mais simples para isso é indicar aos números acima de 26 que eles devem retornar ao início e recomeçar com um índice de 1, e não de 25. 
A maneira mais simples de fazer isso é usar o operador módulo (%).

Consulte o arquivo `ccipher` para obter mais detalhes.

### Segunda solução do algoritmo

Array#rotate: Elimina a necessidade do operador módulo (%) ao deslocar arrays alfabéticos. <br>
String#tr: Realiza substituições de forma eficiente, incluindo caracteres não alfabéticos (que são ignorados).

Consulte o arquivo `cciphertr` para obter mais detalhes.

## Demonstração

### Olá Mundo

#### Codificação

![caesar_cipher_ola_encoding](https://github.com/user-attachments/assets/91095553-eaa2-4986-84b2-d733cba1f9ff)

#### Decodificação

![caesar_cipher_ola_decoding](https://github.com/user-attachments/assets/1ba02c08-f6ce-42bc-b61d-1b6a3e5288cf)

### O valor padrão do deslocamento é 1

![caesar_cipher_default_shift_value](https://github.com/user-attachments/assets/1b482944-50b6-4161-a96f-f5ffc26d4eb4)

## Trabalhando com Arquivos

### Substituição de Comando

Codificando um arquivo.

```bash
ccipher "$(cat loremipsum.txt)" 3
```

Codificando um arquivo e criando um novo.

```bash
ccipher "$(cat loremipsum.txt)" 3 > loremipsum-encoded.txt
```

### XARGS

Codificando um arquivo.

```bash
cat loremipsum.txt | xargs -0 -i ccipher {} 3
```

Codificando um arquivo e criando um novo.

```bash
cat loremipsum.txt | xargs -0 -i ccipher {} 3 > loremipsum-encoded.txt
```

## Mostre seu apoio

Por favor, marque com ⭐️ este repositório se você gostou!

## Autor

- GitHub: [@GuilhermeCCunha](https://github.com/GuilhermeCCunha)

[readme-en]: https://github.com/GuilhermeCCunha/Caesar_cipher/blob/main/README.md
[github-img]: https://img.shields.io/github/repo-size/GuilhermeCCunha/Caesar_cipher?logo=github&style=flat-square
[github-url]: https://github.com/GuilhermeCCunha/Caesar_cipher
[github-commit]: https://img.shields.io/github/last-commit/GuilhermeCCunha/Caesar_cipher?logo=github&style=flat-square
[ruby]: https://badgen.net/badge/icon/ruby?icon=ruby&label
[ruby-lang]: https://ruby-lang.org/
