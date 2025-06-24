# ➡️↔️🔄 Logica de programação

Este repositório é onde compartilho um pouco do que sei sobre lógica de programação.  
Não sou um expert na área, mas sempre tento focar meus estudos nessa parte, que considero essencial.  
E bom... Aqui é sobre o que eu sei.

---

## ➡️ Lógica Sequencial

Essa é uma das lógicas mais simples, mas conhecer ela a fundo faz total diferença.  
Ela é essencial para entender como estruturar o código e principalmente a importância da indentação.
No meu caso, essa lógica me ajudou a entender como declarar variáveis e reconhecer seus tipos.

### 🧪 Tipos primitivos:
- `int` → números inteiros  
- `float` / `double` → números reais  
- `char` / `string` → caracteres e textos  
- `bool` → valores booleanos (`true` ou `false`)

## 💻 Exemplo prático em C:

```c
#include <stdlib.h>
#include <stdio.h>

int main(){
    char nome[10];
        printf("Digite o nome: ");
            fgets(nome /* variável */, 10 /* Tamanho */,  stdin/* ponteiro do tipo *FILE */);
            /* Variável */nome[/* Função strcspn serve para iterar sobre o valor para encontrar o caractere*/strcspn(nome, "\n")] = '\0'/* Caractere \n*/;

        printf("Nome: %s\n", nome);
}
```

---

### ↔️ Lógica Condicional

A lógica condicional é essencial para criar **rotas** no código.  
Pensa numa cidade com várias ruas: cada rua tem uma condição única que te faz escolher por onde seguir.
Essa lógica me fez enxergar o código como um sistema de **estados**.  
Por que estados? Simples: quando uma condição é atendida, o programa entra em um fluxo específico **um estado diferente** do anterior.
Isso muda tudo, porque você percebe que não é só “verdadeiro ou falso”, mas sim **"pra onde o programa vai"** dependendo da situação.

## 💻 Exemplo prático em C:
### Lógica sequencial composta:

```c
#include <stdio.h>
#include <stdlib.h>

int main(){
    int x;
    /* Lógica de Ifs sequencial composta*/
    printf("Digite o valor de x: ");
        scanf("%d", &x);
    if(x >= 0 && x < 20){
        printf("O valor de 'x' é maior que 0 e menor que 20\n");
    }
    else{
        printf("O valor de 'x' é maior ou igual a 20 e menor que 30\n");
    }
    if(x >= 30){
        printf("O valor de 'x' é maior 30\n");
    }
    else{
        printf("O valor de 'x' é menor que 30\n");
    }
}
```

---

# 🔄 Lógica de Repetição

Essa lógica é muito interessante eu costumo pensar nela como o **ciclo da vida**.  
Temos um ponto de entrada, onde um valor começa a percorrer até atingir um determinado limite (`x`).  
E quem faz isso acontecer é o **contador**, que percorre esse trajeto até o fim.
É uma das lógicas que eu mais gosto.  
Se você parar pra analisar, isso nada mais é do que um **percurso a ser corrido**, e o código é quem guia esse caminho.

## 💻 Exemplo prático em C:
### Lógica repetição pós-teste(do-while):

```c
#include <stdio.h>
#include <stdlib.h>

int main(){
    int i = 5;
    int y;
    int x;
    int res;
    char s;
    printf("Digite o valor de x e y: \n");
    do{
        printf("digite o valor x: ");
            scanf("%d", &x);
        printf("digite o valor de y: ");
            scanf("\n%d", &y);
        res =  x * y;
        printf("Resposta: %d\n", res);
        getchar();
        printf("Digite 's' para continuar: ");
            scanf("%c", &s);
        i++;
    }while(s == 's');
}
```

---

# Mapa para entender o contexto:

![alt text](<Mapa mental(1).png>)