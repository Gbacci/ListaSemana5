1) resposta A
2) resposta A
3) resposta A
4) resposta A
5) resposta A
6) resposta A

7)
// Define a classe Animal
class Animal {
    // Construtor da classe Animal
    constructor(nome, idade) {
      this.nome = nome;
      this.idade = idade;
    }
  
    // imprime informações sobre o animal no console
    descrever() {
      console.log(`Este animal é um ${this.nome} e tem ${this.idade} anos de idade.`);
    }
  }
  
  // criando objetos da classe Animal
  const cachorro = new Animal("cachorro", 3); // cachorro com nome "cachorro" e idade 3
  const gato = new Animal("gato", 2);         // gato com nome "gato" e idade 2
  
  // Chama o descrever() para cada animal, exibindo informações no console
  cachorro.descrever(); // Saída: este animal é um cachorro e tem 3 anos de idade.
  gato.descrever();     // Saída: Este animal é um gato e tem 2 anos de idade.
  ```

  8)
 // Define a classe Animal
class Animal {
    // Construtor da classe
    constructor(nome, idade) {
      // Atributos nome e idade da classe
      this.nome = nome;
      this.idade = idade;
    }
  
    // Imprime no console uma mensagem sobre o animal
    descrever() {
      console.log(`Este animal é um ${this.nome} e tem ${this.idade} anos de idade.`);
    }
  }
  
  // Definição da classe Gato que estende a classe Animal
  class Gato extends Animal {
    // Construtor da classe
    constructor(nome, idade, cor) {
      super(nome, idade);
      // Atributo cor da classe
      this.cor = cor;
    }
  
    // Imprime no console a mensagem "Miau!"
    miar() {
      console.log("Miau!");
    }
  }
  
  // Criando objetos das classes Animal e Gato
  const cachorro = new Animal("cachorro", 3);
  const gato = new Gato("gato", 2, "preto");
  
  cachorro.descrever(); // Saída: Este animal é um cachorro e tem 3 anos de idade.
  gato.descrever(); // Saída: Este animal é um gato e tem 2 anos de idade.
  
  gato.miar(); // Saída: Miau!

9)
// define a classe SomadorDeNotas
class SomadorDeNotas {
    // construtor da classe
    constructor() {
      this.total = 0;
    }
  
    // adiciona uma nota ao total
    adicionarNota(nota) {
      this.total += nota;
    }
  
    // exibe o total das notas no console
    verTotal() {
      console.log(`O total das notas é: ${this.total}`);
    }
  }
  
  // cria um objeto da classe SomadorDeNotas
  const somador = new SomadorDeNotas();
  
  // adicionando algumas notas ao somador
  somador.adicionarNota(8);
  somador.adicionarNota(7.5);
  somador.adicionarNota(9);
  
  // chamando o verTotal() para exibir o total das notas
  somador.verTotal(); // Saída: O total das notas é: 24.5

10)
// Define a classe Funcionario
class Funcionario {
    // Construtor da classe
    constructor(nome, idade, salarioBase) {
      this.nome = nome;
      this.idade = idade;
      this.salarioBase = salarioBase;
    }
  
    calcularSalario() {
    }
  }
  
  // Define a classe Professor, que herda de Funcionario
  class Professor extends Funcionario {
    // Construtor da classe
    constructor(nome, idade, salarioBase, disciplina, horasAula) {
      super(nome, idade, salarioBase);
      this.disciplina = disciplina;
      this.horasAula = horasAula;
    }
  
    // Implementação do calcularSalario específico para professores
    calcularSalario() {
      const valorHoraAula = 50;
      const salarioProfessor = this.horasAula * valorHoraAula;
  
      // Adiciona o salário base ao salário calculado
      const salarioTotal = this.salarioBase + salarioProfessor;
  
      // Exibe o resultado no console
      console.log(`O salário do professor ${this.nome} é: R$ ${salarioTotal.toFixed(2)}`);
    }
  }
  
  // Criando dois objetos do tipo Professor
  const professor1 = new Professor("aaa", 35, 2000, "Matemática", 20);
  const professor2 = new Professor("aaaa", 40, 2200, "História", 15);
  
  // Chamando o calcularSalario() para cada objeto e mostra o salário calculado no console
  professor1.calcularSalario(); // Saída esperada: O salário do professor aaa é: R$ 3000.00
  professor2.calcularSalario(); // Saída esperada: O salário do professor aaaa é: R$ 2350.00
