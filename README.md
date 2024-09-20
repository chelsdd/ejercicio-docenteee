package javaapplication33;

import java.util.ArrayList;
import java.util.Scanner;
public class JavaApplication33 {

       public static void main(String[] args) {
       
        
       
        ArrayList<Docente1> docentes = new ArrayList<>();
           try (Scanner scanner = new Scanner(System.in)) {
               
      
        for (int i = 0; i < 5; i++) {
            System.out.println("Ingresa el tipo de docente (1 para HC1, 2 para TCO): ");
            int tipoDocente = scanner.nextInt();
            scanner.nextLine(); 

            System.out.println("Ingresa el nombre del docente: ");
            String nombre = scanner.nextLine();

            System.out.println("Ingresa la facultad del docente: ");
            String facultad = scanner.nextLine();

            System.out.println("Ingresa el CADI del docente: ");
            String cadi = scanner.nextLine();

            if (tipoDocente == 1) {
                
                System.out.println("Ingresa las horas trabajadas: ");
                int horasTrabajadas = scanner.nextInt();

                System.out.println("Ingresa el valor por hora: ");
                double valorhora = scanner.nextDouble();

                
                docentes.add(new DocenteHC1(juan, ingenieria, cadi3, 6, 58));

            } else if (tipoDocente == 2) {
                
                System.out.println("Ingresa el sueldo básico: ");
                double sueldoBasico = scanner.nextDouble();

                System.out.println("Ingresa la cantidad de trabajos de grado: ");
                int cantTrabGrado = scanner.nextInt();

                System.out.println("Ingresa el valor por hora de asesoría: ");
                double valorHoraAsesor = scanner.nextDouble();

                
                docentes.add(new DocenteTCO(nombre, facultad, cadi, sueldoBasico, cantTrabGrado, valorHoraAsesor));
            }
        }

        
        System.out.println("\n--- Datos de los docentes ingresados ---");
        for (Docente1 docente1 : docentes) {
            docente1.mostrarDatos();
            System.out.println(); 
        }

        
        scanner.close();
    }
}

    }
