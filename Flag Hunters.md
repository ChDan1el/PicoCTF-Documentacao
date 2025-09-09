Introdução

Esse desafio é sobre engenharia reversa, mais especificamente a [injeção de código](https://brightsec.com/blog/code-injection/),
tendo como objetivo encontrar a vulnerabilidade no código e aplicar um comando para a obtenção
da flag.

[Página do desafio](https://play.picoctf.org/practice/challenge/472)

Passo a Passo

1-Primeira coisa a se fazer é analisar o código Python e tentar entendê-lo.
A parte que queremos que seja impressa não está sendo retornada porque fica alternando entre refrão e estrofes.

https://ibb.co/Vcbf2C8Q

https://ibb.co/BV3zyRvX

2- Uma maneira de contornar o problema e imprimir o verso oculto é usar o próprio comando "RETURN" do programa, sendo usado para
retornar à linha desejada. Usufruindo da vulnerabilidade do código, já que o input não é devidamente filtrado.

https://ibb.co/cjbKdLZ

3- Usando o comando "palavra";RETURN 9 o programa buga e fica em looping e não imprime o que quero, sendo "palavra" a parte que o programa vai ler como string
e o RETURN 9 o comando que quero injetar.
Então faço outro comando, só que agora voltando à linha 0, "palavra";RETURN 0, dando finalmente certo.

https://ibb.co/C3f0Q9F7

https://ibb.co/F4qh5Yx1

Flag: picoCTF{70637h3r_f0r3v3r_836f0788}

Conclusão:

Esse desafio é bastante difícil para resolver, entretanto ele realça a importância
da segurança no input realizado pelo usuário, oferecendo grandes riscos à funcionalidade
do programa e o comprometimento de dados internos.



