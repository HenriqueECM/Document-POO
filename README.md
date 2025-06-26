# 🧠 Programação Orientada a Objetos

## 📚 Sumário
- [📖 Introdução](#-introdução)
- [❓ O que é Programação Orientada a Objetos?](#-o-que-é-programação-orientada-a-objetos)
- [📦 O que são Objetos?](#-o-que-são-objetos)
- [🏫 O que são Classes?](#-o-que-são-classes)
- [🧩 Os 4 Pilares da Programação Orientada a Objetos](#-os-4-pilares-da-programação-orientada-a-objetos)
  - [🔒 Encapsulamento](#-encapsulamento)
  - [🧬 Herança](#-herança)
  - [🎭 Polimorfismo](#-polimorfismo)
  - [🧱 Abstração](#-abstração)
- [🏗️ Construtores](#️-construtores)
- [🔄 Sobrecarga (Overloading)](#-sobrecarga-overloading)
- [🔁 Sobrescrita (Overriding)](#-sobrescrita-overriding)
- [📌 Comparativo Rápido](#-comparativo-rápido)

---

## 📖 Introdução
Esta documentação foi elaborada com o objetivo de organizar e aprofundar meus estudos sobre **Programação Orientada a Objetos (POO)**.

Considerando que a POO é um paradigma essencial para o desenvolvimento de sistemas estruturados, reutilizáveis e de fácil manutenção, torna-se fundamental compreender seus conceitos e aplicá-los de forma consistente.

Por meio deste material, busco consolidar conhecimentos que possibilitem a construção de softwares mais robustos e profissionais, ampliando minha capacidade técnica e preparando-me para desafios práticos na área de desenvolvimento de sistemas.

---

## ❓ O que é Programação Orientada a Objetos?
É um **paradigma de programação** que organiza o código em torno de **objetos**, que são entidades que combinam **dados (atributos)** e **ações (métodos)**.

Esse modelo se aproxima da forma como representamos o mundo real, facilitando a modelagem e manutenção dos sistemas.

---

## 📦 O que são Objetos?
Um **objeto** é uma **instância de uma classe**.

Ao criar um objeto, estamos gerando um “exemplar” daquela classe, com **seus próprios valores para os atributos** e a capacidade de executar os **métodos definidos na classe**.

---

## 🏫 O que são Classes?
Uma **classe** é um **molde** ou estrutura que define os **dados (atributos)** e **comportamentos (métodos)** de um tipo de objeto.

Ela serve como uma **base para criar objetos**, determinando quais informações e ações estarão disponíveis em cada instância.

---

## ⚙️ O que são Métodos?
São funções definidas dentro de uma classe, onde descrevem ações que um objeto dessa classe pode realizar.

---

## 🧩 Os 4 Pilares da Programação Orientada a Objetos

A Programação Orientada a Objetos se apoia em **quatro pilares fundamentais**, que são os responsáveis por tornar esse paradigma tão poderoso e versátil:

---

### 🔒 Encapsulamento

O **encapsulamento** é um dos pilares da Programação Orientada a Objetos.  
Ele consiste em **ocultar os detalhes internos** de um objeto e expor apenas o necessário para seu uso externo.

Os dados são protegidos por **modificadores de acesso** (`private`, `public`, etc.) e manipulados por **métodos acessores** (`get` e `set`), garantindo:

- ✅ Segurança dos dados  
- ✅ Controle sobre as alterações  
- ✅ Organização e clareza no código  

---

#### 🧰 Métodos Get e Set

Os métodos `get` e `set` são utilizados para **acessar e modificar atributos privados** de uma classe.  
Dessa forma, os atributos não são alterados diretamente, mas sim através de métodos controlados.

#### Exemplo:
```java
public class Carro {
    private String marca;

    // Método GET: retorna o valor do atributo
    public String getMarca() {
        return nome;
    }

    // Método SET: altera o valor do atributo com validação
    public void setMarca(String marca) {
        this.marca = marca;
    }
}
```
#### 📌 Com esse padrão:

- É possível aplicar validações e regras de negócio antes de alterar dados.

- Evita-se a exposição direta de atributos sensíveis.

#### 🔒 Modificadores de Acesso
Os modificadores de acesso controlam a visibilidade de classes, atributos e métodos.

| Modificador | Acesso permitido a:                |
| ----------- | ---------------------------------- |
| `private`   | Apenas dentro da **mesma classe**  |
| `protected` | Na classe e em **subclasses**      |
| `public`    | Qualquer classe (acesso **total**) |
| *(default)* | Classes do **mesmo pacote** (Java) |

#### ✅ Benefícios do Encapsulamento
- 🧱 Organização e modularidade do código
- 🛡️ Proteção contra dados inválidos ou inconsistentes
- 🔄 Facilidade para manutenção e evolução do sistema
---

### 🧬 Herança  
Permite que uma **classe herde atributos e métodos** de outra classe, promovendo **reutilização de código** e facilitando a **especialização de comportamentos** (métodos).  
➡️ A classe herdada é chamada de **superclasse**, e a que herda é chamada de **subclasse**.

---

### 🎭 Polimorfismo  
Significa “**muitas formas**”. Permite que um mesmo método tenha comportamentos diferentes, dependendo do objeto que o invoca.  
➡️ Pode ocorrer por **sobrecarga** (mesmo nome, diferentes parâmetros) ou **sobrescrita** (reescrever método da superclasse).

---

### 🧱 Abstração  
Consiste em **representar conceitos complexos** do mundo real de forma simplificada, focando apenas nos **aspectos essenciais**.  
➡️ Isso reduz a complexidade do sistema e facilita o entendimento e a manutenção do código.

---

## 🏗️ Construtores

Um **construtor** é um método especial utilizado para **inicializar objetos** de uma classe.

- Tem o **mesmo nome da classe**.
- **Não possui tipo de retorno** (nem `void`).
- É automaticamente chamado ao instanciar o objeto com `new`.

### 🧪 Exemplo:
```java
public class Pessoa {
    private String nome;
    private int idade;

    // Construtor
    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    public void apresentar() {
        System.out.println("Olá, meu nome é " + nome + " e tenho " + idade + " anos.");
    }
}
```
---

## 🔄 Sobrecarga (Overloading)
A sobrecarga ocorre quando métodos com o mesmo nome têm parâmetros diferentes (tipo, quantidade ou ordem).

Isso permite que um mesmo método se comporte de várias formas, dependendo dos argumentos passados.

### 🧪 Exemplo:
```java
public class Calculadora {

    public int somar(int a, int b) {
        return a + b;
    }

    public double somar(double a, double b) {
        return a + b;
    }

    public int somar(int a, int b, int c) {
        return a + b + c;
    }
}
```
### ▶️ uso
```java
Calculadora calc = new Calculadora();
calc.somar(2, 3);         // int
calc.somar(2.5, 3.5);     // double
calc.somar(1, 2, 3);      // três inteiros
```
---

## 🔁 Sobrescrita (Overriding)
A sobrescrita ocorre quando uma subclasse reimplementa um método herdado da superclasse com um novo comportamento.

- A assinatura do método deve ser idêntica à original.
- Usa-se a anotação @Override por boas práticas.

### 🧪 Exemplo:
```java
class Animal {
    public void emitirSom() {
        System.out.println("O animal faz um som.");
    }
}

class Cachorro extends Animal {
    @Override
    public void emitirSom() {
        System.out.println("O cachorro late.");
    }
}
```
### ▶️ uso
```java
Animal a = new Animal();
a.emitirSom();  // O animal faz um som.

Animal c = new Cachorro();
c.emitirSom();  // O cachorro late.
```
---
### 📌 Comparativo Rápido
| Conceito    | Característica Principal                              | Ocorre onde?                  |
| ----------- | ----------------------------------------------------- | ----------------------------- |
| Sobrecarga  | Mesmo nome, diferentes parâmetros                     | Mesma classe                  |
| Sobrescrita | Mesmo nome, mesma assinatura, comportamento diferente | Entre superclasse e subclasse |
