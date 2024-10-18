# Estudo de comandos NASM

<p align="center">

<img src="https://seeklogo.com/images/N/netwide-assembler-nasm-logo-EC5B1109AC-seeklogo.com.png " width=200 heigh=200 >

</p>
## primeiros comandos


* Programa hello word
 
  ```Assembly

 
 global _start

        section .text
        _start:
            mov rax,1        ;Prepara o sistema
            para fazer a escrita de um texto
            mov rdi,1        ;Prapara a saida do texto na tela
            mov rsi,mensagem ;Imprimir a mensagem na tela
            mov rdx,13       ;Quantidade de caracteres
            syscall          ;chama o sistema para preparar a saída
            mov rax,60       ;chamada para a saída do sistema
            xor rdi,rdi      ;executar a saída o sistema
            syscall          ;invocar o sistema operacional para fechar

            section .data
            mensagem:db 'Hello,world',10 ;O valor 10 representa quebra de linha 

```