# PorcentajeMujeres
cálculo de mujeres inscritas
import java.util.Scanner;

public class PorcentajeMujeres {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");

        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Introduce el número total de candidatos: ");
            int total = Integer.parseInt(scanner.nextLine());

            System.out.print("Introduce el número de mujeres inscritas: ");
            int mujeres = Integer.parseInt(scanner.nextLine());

            double porcentaje = calcularPorcentajeMujeres(total, mujeres);
            System.out.printf("Porcentaje de mujeres: %.2f%%\n", porcentaje);
        } catch (NumberFormatException e) {
            System.out.println("Por favor, introduce solo números enteros válidos.");
        }

        scanner.close();
    }

    public static double calcularPorcentajeMujeres(int totalCandidatos, int mujeresInscritas) {
        if (totalCandidatos == 0) {
            return 0; // Evita división por cero
        }
        return ((double) mujeresInscritas / totalCandidatos) * 100;
    }
}
