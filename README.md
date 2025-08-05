# Meu ft_printf - Projeto 42 (Standalone)

![C](https://img.shields.io/badge/Language-C-blue.svg)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![42 School](https://img.shields.io/badge/School-42%20SP-black)

O `ft_printf` é um projeto da escola 42 que consiste em recriar a famosa função `printf` da biblioteca padrão do C. Este projeto aprofunda os conhecimentos sobre funções variádicas em C.

Esta implementação é totalmente autossuficiente (standalone) e não requer a `libft` ou qualquer outra biblioteca externa para funcionar.

## ✨ Conversores Suportados

| Conversor | Descrição                               |
| :-------: | ----------------------------------------- |
|    `c`    | Imprime um único caractere.               |
|    `s`    | Imprime uma string (cadeia de caracteres).|
|    `p`    | Imprime o endereço de um ponteiro em hexadecimal. |
|    `d`    | Imprime um número decimal (base 10).      |
|    `i`    | Imprime um inteiro em base 10.            |
|    `u`    | Imprime um número decimal sem sinal.      |
|    `x`    | Imprime um número em hexadecimal (letras minúsculas). |
|    `X`    | Imprime um número em hexadecimal (letras maiúsculas). |
|    `%`    | Imprime o símbolo de porcentagem (`%`).   |

*(Opcional: se você fez o bônus, pode adicionar uma seção para as flags que implementou, como `'-', '0', '.', '#', ' '` e `'+'`)*

## ⚙️ Como Compilar e Usar

**1. Compilar a biblioteca**

Para compilar e criar o arquivo de biblioteca estática (ex: `libftprintf.a`), execute o `Makefile` na raiz do projeto:

```bash
make
```
Isso irá gerar o arquivo de biblioteca `libftprintf.a`.

**2. Usar `ft_printf` em um projeto**

Crie um arquivo de exemplo, como `meu_programa.c`, e inclua o cabeçalho `ft_printf.h`:

```c
#include "ft_printf.h"

int main(void)
{
    char *nome = "Mundo";
    int ano = 2024;
    
    ft_printf("Olá, %s!\n", nome);
    ft_printf("Estamos no ano de %d.\n", ano);
    ft_printf("Um número em hexadecimal: %x\n", 12345);
    ft_printf("Imprimindo um percentual: 100%%\n");
    
    return (0);
}
```

Para compilar o seu programa, você só precisa linkar a biblioteca `ft_printf`:

```bash
# Onde -L. indica para o compilador procurar a biblioteca no diretório atual
# E -lftprintf diz para linkar com a biblioteca 'libftprintf.a'
gcc meu_programa.c -L. -lftprintf -o meu_programa
```

Depois, execute o seu programa:
```bash
./meu_programa
```

## 👤 Autor

**Claudio Matheus**

* Github:  @claudio1code (https://github.com/claudio1code)
* Login 42: `clados-s`
