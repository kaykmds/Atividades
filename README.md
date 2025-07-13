 java.util.Scanner;

public class CalculoMedias {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Receber as notas do aluno
        System.out.println("Digite as 8 notas anuais:");
        double[] notas = new double[8];
        for (int i = 0; i < 8; i++) {
            System.out.print("Nota " + (i + 1) + ": ");
            notas[i] = scanner.nextDouble();
        }

        // Calcular as médias bimestrais
        double mediaBimestral1 = (notas[0] + notas[1]) / 2;
        double mediaBimestral2 = (notas[2] + notas[3]) / 2;
        double mediaBimestral3 = (notas[4] + notas[5]) / 2;
        double mediaBimestral4 = (notas[6] + notas[7]) / 2;

        // Calcular as médias semestrais
        double mediaSemestral1 = (mediaBimestral1 + mediaBimestral2) / 2;
        double mediaSemestral2 = (mediaBimestral3 + mediaBimestral4) / 2;

        // Calcular a média final
        double mediaFinal = (mediaSemestral1 + mediaSemestral2) / 2;

        // Apresentar os resultados
        System.out.println("\nResultados:");
        System.out.println("Médias Bimestrais:");
        System.out.println("1º Bimestre: " + mediaBimestral1);
        System.out.println("2º Bimestre: " + mediaBimestral2);
        System.out.println("3º Bimestre: " + mediaBimestral3);
        System.out.println("4º Bimestre: " + mediaBimestral4);
        System.out.println("\nMédias Semestrais:");
        System.out.println("1º Semestre: " + mediaSemestral1);
        System.out.println("2º Semestre: " + mediaSemestral2);
        System.out.println("\nMédia Final: " + mediaFinal);
    }
}
