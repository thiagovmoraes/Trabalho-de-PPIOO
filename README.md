Trabalho-de-PPIOO
=================

Atualização do código referente ao jogo RPG da matéria PPIOO, ministrada pela professora Valéria.


/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package trabalhoppioo;

import java.util.Scanner;

class Personagem
{
    String nome;
    int quantidadeVida;
    int dano;    
    int resistencia;
    
    public int getDano()    {
        return dano;
    }
    
    public int getResistencia(){
        return resistencia;
    }
    
}


class Antagonista extends Personagem
{
    String atacar(Personagem x)
    {
        x.quantidadeVida = x.quantidadeVida - getDano()*2;        
        return null;
    } 
}
    
class Protagonista extends Personagem
{
    int fatorIncremento;
    String atacar(Personagem x)
    {
        x.quantidadeVida = x.quantidadeVida - getDano();
        return null;
    }
}



public class Trabalhoppioo {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       
        Antagonista t = new Antagonista();
        t.nome = "tigrinho";
        t.quantidadeVida = 100;
        t.dano = 10;
        t.resistencia = 10;
        
        Protagonista a = new Protagonista();
        a.nome = "amanda";
        a.quantidadeVida = 100;
        a.dano = 8;  
        a.resistencia = 8;
        
        Protagonista b = new Protagonista();
        b.nome = "Macaco americano";
        b.quantidadeVida = 100;
        b.dano = 50;
        b.resistencia = 20;
      
        
        /** System.out.println("A quantidade de vida de " + t.nome + ", é de: " + a.quantidadeVida);
        System.out.println("A quantidade de vida de " + a.nome + ", é de: " + t.quantidadeVida);
        
        while (a.quantidadeVida > 0 && t.quantidadeVida > 0)
        {
            t.atacar(b);
            System.out.println(t.nome + " atacou " + a.nome);
            System.out.println("A quantidade de vida de " + a.nome + ", é de: " + a.quantidadeVida);
            a.atacar(t);
            System.out.println(a.nome + " atacou " + t.nome);
            System.out.println("A quantidade de vida de " + t.nome + ", é de: " + t.quantidadeVida);            
        }       
        if (a.quantidadeVida <= 0)
            {
                System.out.println(t.nome + " venceu...");                
            }
        else if (t.quantidadeVida <= 0)
            {
                System.out.println(a.nome + " venceu...");
            } */
    }
}
