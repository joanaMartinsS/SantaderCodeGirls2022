# Conceituação e Criação de Variáveis

## Conceituação
* É um espaço na memória do computador, onde se pode guardar valores
* Tipos de Variáveis:
    * Variável instância: pertence a um objeto;
    * Variável classe: pertence a uma classe;
    * Variável local: dentro de métodos    
    * Variável parâmetro: na assinatura de métodos.

## Criação
* Padrão de definição: visibilidade modificador tipo nome valor inicial;
    * Visibilidade: public, protected e private;
    * Modificador: static e final (o valor não muda);
    * Tipo de dado (é obrigatório): int, double, string e etc;
    * Nome (é obrigatório);
    * Valor inicial.

* Convenção e regras:
    * Não pode iniciar com número;
    * Não é uma boa prática utilizar "$" e "_";
    * São case-sensitive (diferencia maiúsculas com minúsculas);
    * Não pode utilizar as palavras reservadas do Java;
    * Não se pode utilizar caracteres especiais;
    * Não pode ter o mesmo nome que outra variável;
    * Variáveis dentro de métodos precisam ter valor inicial.

* Boas práticas:
    * Sempre começar com letra minúscula;
    * Nomes expressivos;
    * Notação camelo;
    * Quando a variável for constante (final) seu nome deve ser maiúsculo e separado por "_".

# Tipos de Dados
## Conceituação
* Tipificação:
    * Estática ou forte (é obrigatório definir o tipo de dado e esse tipo não muda) ou dinâmica ou fraca (não é obrigatório definir o tipo de dado e esse tipo pode mudar);
    * Primitivo (valores numéricos, textuais, os tipos mais básicos) ou composto (está ligado a POO, composto de vários tipos de dados primitivos ou de tipos compostos. Ex.: String).

* Os tipos de dados podem ser textuais, numerais, lógicos ou objetos;

## Utilização:
* Numerais:
    * byte: -128 até 127; inteiro
    * short: -32.768 até 32.767; inteiro
    * int: -2.147.483.648 até 2.147.483.647, inteiro de 32 bits;
    * long: muito maior, inteiro de 64 bits; (prcisa escrever L no final se não o Java entende como int)
    * float: fracionados de 32 bits; (precisa escrever f no final do número se não ele vai ser double) ex.: 3.14f
    * double: fracioados de 64 bits; ex.: 3.14d aqui essa explicitação é opicional

* Textuais:
    * char: caracteres de 16-bits unicode, caracteres ASCII
    * String: um tipo especial, são os textos. Na realidade String é um objeto de uma classe do Java.
    * OBS.: para caracter unitário utiliza-se aspas simples e para conjunto de caracteres utiliza-se aspas duplas. Ex.: "Texto" e 'T'

* Lógicos:    
    * boolean: true or false

* Boas práticas: Usar de forma adequada cada tipo de dado para cada informação.

# Operadores Aritméticos
## Conceituação
* São simbolos especiais que realizam operações tipo soma, subtração, divisão inteira, resto da divisão e etc.
* Tipos:
    * Pós-fixado: exp++ ou exp--. Soma uma unidade ou subtrai após a expressão; ex.: int i = ++k siginifica i = k + 1;
    * Préfixado: ++exp ou --exp. Soma uma unidade ou subtrai antes da expressão; ex.: int j = k-- significa j = k; k = k-1;
    * Aritmético: +, -, *, / e %;
    * Atribuição: =, +=, -= e %=;

* Prioridades de Execução
    * Pós-fixado: exp++, exp--
    * Pre-fixado: ++exp, --exp
    * Multiplicativo: *, /, %
    * Aditivo: +, -
    * Atribuição: =, +=, -=, /=, %=

# Conversões
# Conceituação 
* Transformação de uma determinada variável de tipo menos específico para mais específico ou vice-versa. Subir ou diminuir a capacidade de armazenamento.
* Tipos:
    * Upcast(implícito): tipo menos específico para maior;
    * Downcast(explícito): tipo mais específico para menor.
* Exemplos:
    * long I; int i = 10; I = i; (Upcast);
    * int i long I = 100; i = (int) i; (Downcast sem perda de dados);
    * int i; float b = 10.5f; int = (int) b; (Downcast com perda de dados);

    