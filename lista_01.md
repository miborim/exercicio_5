# Instruções

- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

A) Imprime os números pares de 1 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota");

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

A) 18

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

A) ![Uma imagem](assets/ex04_1.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

A) "Olá, meu nome é João. Olá, meu nome é Maria."

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

**Resposta:**
class Animal {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  descrever() {
    console.log(`Este é o ${this.nome} e ele tem ${this.idade} anos!`);
  }
}

const gato = new Animal("Tito", "3");
gato.descrever();

const cachorro = new Animal ("Beto", "5");
cachorro.descrever();

______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

**Resposta:**
class Animal {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  descrever() {
    console.log(`Este é o ${this.nome} e ele tem ${this.idade} anos!`);
  }
}

class Gato extends Animal {
  constructor(nome, idade, cor) {
    super(nome, idade);
    this.cor = cor;
  }
    console.log(`A cor dele é ${this.cor}.`);

  miar() {
    console.log(`A cor dele é ${this.cor}.`,`\nO som que o ${this.nome} faz é "miau"!`);
  }
}

const cachorro = new Animal ("Beto", "5");
cachorro.descrever();

const gato = new Gato ("Tito", "3", "preta");
gato.descrever();
gato.miar();

______

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

// Definindo a classe SomadorDeNotas
class SomadorDeNotas {
  // Definindo construtor da classe, chamado a cada objeto criado
  constructor() {
    // Inicializando o atributo total com o valor zero
    this.total = 0;
  }

  // Método para adicionar uma nota ao total
  adicionarNota(nota) {
    // Incrementando o total com o valor da nota fornecida
    this.total += nota;
  }

  // Método para exibir o total das notas no console
  verTotal() {
    // Exibindo uma mensagem com o valor total
    console.log(`A soma total das notas é igual a ${this.total}.`);
  }
}

// Criando uma instância da classe SomadorDeNotas, um objeto chamado somador
const somador = new SomadorDeNotas();

// Adicionando notas ao somador
somador.adicionarNota(7);
somador.adicionarNota(8);
somador.adicionarNota(6);

// Exibindo o total das notas no console
somador.verTotal();


______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

// Definindo a classe Funcionario
class Funcionario {
  // Definindo construtor da classe Funcionario que recebe os atributos nome, idade e salário base
  constructor(nome, idade, salarioBase) {
    // Atribuindo os atributos
    this.nome = nome;
    this.idade = idade;
    this.salarioBase = salarioBase;
  }

  // Definindo método calcularSalario
  calcularSalario() {
  }
}

// Definindo a classe Professor, que herda de Funcionario
class Professor extends Funcionario {
  // Definindo construtor da classe Professor
  constructor(nome, idade, salarioBase, disciplina, horasAula) {
    // Chamando o construtor da classe pai usando super()
    super(nome, idade, salarioBase);
    // Atribuindo os atributos específicos da classe Professor
    this.disciplina = disciplina;
    this.horasAula = horasAula;
  }

  // Sobrescrevendo o método calcularSalario da classe pai
  calcularSalario() {
    // Calculando o salário do professor multiplicando as horas de aula pelo salário base
    this.salario = this.salarioBase * this.horasAula;
  }
}

// Criando duas instâncias da classe Professor com informações fictícias
const professor1 = new Professor("Mário", "42 anos", "100", "História", 10);
const professor2 = new Professor("Joana", "38 anos", "120", "Matemática", 16);

// Chamando o método calcularSalario para cada objeto Professor
professor1.calcularSalario();
professor2.calcularSalario();

// Exibindo informações sobre cada professor no console
console.log(`${professor1.nome} leciona ${professor1.disciplina} e seu salário é de R$${professor1.salario}.`);
console.log(`${professor2.nome} leciona ${professor2.disciplina} e seu salário é de R$${professor2.salario}.`);