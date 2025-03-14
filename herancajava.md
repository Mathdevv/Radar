
package com.mycompany.heranca;

// Classe base (superclasse)
class Animal {
    protected String nome;
    protected int idade;

    public Animal(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    public void falar() {
        System.out.println(nome + " esta falando.");
    }
}

// Subclasse cachorro
class Cachorro extends Animal {
    public Cachorro(String nome, int idade) {
        super(nome, idade);
    }

    public void latir() {
        System.out.println(nome + " esta latindo muito.");
    }
}

// Subclasse gato
class Gato extends Animal {
    public Gato(String nome, int idade) {
        super(nome, idade);
    }

    public void miar() {
        System.out.println(nome + " esta miando.");
    }
}

// Classe principal para testar a herança
public class Heranca {
    public static void main(String[] args) {
        Cachorro cachorro = new Cachorro("Jeferson", 5);
        Gato gato = new Gato("Lua", 3);

        cachorro.falar();
        cachorro.latir();

        gato.falar();
        gato.miar();
    }
}
