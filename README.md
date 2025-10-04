# portfolio
proyectos
Proyecto de calcular la fuerza tipeando la masa y aceleración en el main del código. Java 
//1. clase Fuerza
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package fuerza;

/**
 *
 * @author Emily
 */
public class Fuerza {
    private  double masa;
    private double aceleracion;

    public Fuerza(double masa, double aceleracion) {
        this.masa = masa;
        this.aceleracion = aceleracion;
    }

    public double getMasa() {
        return masa;
    }

    public double getAceleracion() {
        return aceleracion;
    }
    public double calculoFuerza(){
        return masa*aceleracion;
    }
   @Override
    public String toString() {
        return "Fuerza{masa=" + masa + ", aceleracion=" + aceleracion + '}';
    }
}
// 2. clase RegistroFuerza
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package fuerza;

import java.util.ArrayList;

/**
 *
 * @author emily
 */
public class RegistroFuerza {
    private ArrayList<Fuerza>fuerza;

    public RegistroFuerza() {
        this.fuerza= new ArrayList<>();
    }
    public void  cargaFuerza(Fuerza f){
        this.fuerza.add(f);
    }
    public double mayorFuerza(){
        double mayor=0;
        for (Fuerza f: fuerza){
            if(f.calculoFuerza()>mayor){
                mayor= f.calculoFuerza();
            }
        }
        return mayor; 
    }
    public void mostrar (){
        for (Fuerza fuerza : fuerza) {
            System.out.println("Masa: " + fuerza.getMasa() + ", Aceleración: " + fuerza.getAceleracion() + ", Fuerza: " + fuerza.calculoFuerza());
        }
    }       
}    
// 3. Main, Clase Principal
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package fuerza;

import java.util.ArrayList;
/**
 *
 * @author emily
 */
public class Principal {
    public static void main(String[] args) {
        RegistroFuerza f= new RegistroFuerza();
        ArrayList<Fuerza> arraylist= new ArrayList<>();
        //System.out.println(arraylist);
       f.cargaFuerza(new Fuerza(5,7));
       f.cargaFuerza (new Fuerza(7,8));
        
        System.out.println("La fuerza mayor: " + f.mayorFuerza());
        f.mostrar();
        
        //ArrayList<Fuerza> arraylist= new ArrayList<>();
        
        /*System.out.println(arraylist.size());
        System.out.println(arraylist);*/
        //System.out.println(arraylist.addAll(f.cargaFuerza()));
        //System.out.println(f.cargaFuerza(f));
       // double masa=0;
        /*do{
            f.cargaFuerza(new Fuerza(masa, aceleracion));
        
           // f.cargaFuerza(new Fuerza (5,7));
            //System.out.println("la masa debe ser mayor o igual que cero");
         //System.out.println("La fuerza es: " + fuerza.calculoFuerza());
        }while(masa>0);*/
        
    }
}
    
                
