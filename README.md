# lanchonete
Código simples lanchonete


import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        boolean opcaoValida = false;
        int opcao = 0;
        int quantidade = 0;

        while (!opcaoValida) {
            System.out.println("Olá, tudo bem?! O que deseja?");
            System.out.println("Opção [1] = Cachorro Quente. R$ 4.00.");
            System.out.println("Opção [2] = X-Salada. R$ 4.50.");
            System.out.println("Opção [3] = X-bacon. R$ 5.00.");
            System.out.println("Opção [4] = Torrada simples. R$ 2.00.");
            System.out.println("Opção [5] = Refrigerante. R$ 1.50.");

            System.out.println("Digite o código de acordo com seu desejo:");
            opcao = sc.nextInt();

            if (opcao >= 1 && opcao <= 5) {
                opcaoValida = true;
                System.out.println("Opção escolhida: " + opcao);
            } else {
                System.out.println("Opção inválida, digite novamente.");
            }
        }

        System.out.println("Digite a quantidade que você deseja: ");
        quantidade = sc.nextInt();

        double valor_total = 0;

        switch (opcao) {
            case 1:
                valor_total = 4.00 * quantidade;
                System.out.println("Sua opção foi cachorro quente. O total foi " + valor_total);
                break;
            case 2:
                valor_total = 4.50 * quantidade;
                System.out.println("Sua opção foi X-Salada. O total foi " + valor_total);
                break;
            case 3:
                valor_total = 5.00 * quantidade;
                System.out.println("Sua opção foi X-bacon. O total foi " + valor_total);
                break;
            case 4:
                valor_total = 2.00 * quantidade;
                System.out.println("Sua opção foi Torrada simples. O total foi " + valor_total);
                break;
            case 5:
                valor_total = 1.50 * quantidade;
                System.out.println("Sua opção foi Refrigerante. O total foi " + valor_total);
                break;
        }

        System.out.println("Deseja algo a mais? (sim/não)");
        String segunda_opcao = sc.next();

        if (segunda_opcao.equalsIgnoreCase("sim")) {
            System.out.println("O que deseja?");
            System.out.println("Opção [1] = Cachorro Quente. R$ 4.00.");
            System.out.println("Opção [2] = X-Salada. R$ 4.50.");
            System.out.println("Opção [3] = X-bacon. R$ 5.00.");
            System.out.println("Opção [4] = Torrada simples. R$ 2.00.");
            System.out.println("Opção [5] = Refrigerante. R$ 1.50.");
            System.out.println("Digite o código de acordo com seu desejo:");
            int opcao_2 = sc.nextInt();

            System.out.println("Digite a quantidade que você deseja para a opção adicional: ");
            int quantidade_opcao_2 = sc.nextInt();

            double valor_opcao_2 = 0;

            switch (opcao_2) {
                case 1:
                    valor_opcao_2 = 4.00 * quantidade_opcao_2;
                    System.out.println("Sua opção adicional foi cachorro quente. O total foi " + valor_opcao_2);
                    break;
                case 2:
                    valor_opcao_2 = 4.50 * quantidade_opcao_2;
                    System.out.println("Sua opção adicional foi X-Salada. O total foi " + valor_opcao_2);
                    break;
                case 3:
                    valor_opcao_2 = 5.00 * quantidade_opcao_2;
                    System.out.println("Sua opção adicional foi X-bacon. O total foi " + valor_opcao_2);
                    break;
                case 4:
                    valor_opcao_2 = 2.00 * quantidade_opcao_2;
                    System.out.println("Sua opção adicional foi Torrada simples. O total foi " + valor_opcao_2);
                    break;
                case 5:
                    valor_opcao_2 = 1.50 * quantidade_opcao_2;
                    System.out.println("Sua opção adicional foi Refrigerante. O total foi " + valor_opcao_2);
                    break;
            }
            valor_total += valor_opcao_2;
        }

        System.out.println("O valor total a pagar é: R$" + valor_total);
        sc.close();
    }
}
