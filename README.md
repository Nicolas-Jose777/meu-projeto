# meu-projeto
projeto feito com o intuito de dizer quantas e quais tipos de notas devem ser entregues de troco

import java.util.Scanner;

public class Uni3Exe16 {

    public static void main(String[]args) {
        Scanner teclado = new Scanner(System.in);

        int camisa = 87;
        int calca = 120;
        int tenis = 158;
        int assessorio = 53;

        System.out.println("Camisas compradas: ");
        int camisas = teclado.nextInt();
        
        System.out.println("Calças compradas: ");
        int calcas = teclado.nextInt();
        
        System.out.println("Tênis comprados: ");
        int tenisComprados = teclado.nextInt();
        
        System.out.println("Acessórios comprados: ");
        int acessorios = teclado.nextInt();

        int valorTotal = (camisa * camisas) + (calca * calcas) + (tenis * tenisComprados) + (assessorio * acessorios);
        System.out.println("Valor total da compra: R$" + valorTotal);
        
        System.out.println("Deposito o pagamento: ");
        int pagamento = teclado.nextInt();
        
        int valorTroco = pagamento - valorTotal;
        System.out.println("Valor do troco: R$" + valorTroco);

        int cem = valorTroco / 100;
        int dez = (valorTroco % 100) / 10;
        int um = valorTroco % 10;
        int troco = cem + dez + um;

        System.out.println("O número minimo de notas de troco é: " + troco);
        System.out.println("Quantidade de notas de 100: " + cem);
        System.out.println("Quantidade de notas de 10: " + dez);
        System.out.println("Quantidade de notas de 1: " + um);
        teclado.close();
    }
    
}
