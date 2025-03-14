//Radar de velocidade


public class Carro {
    // Atributos do carro
    private String modelo;
    private int velocidade;
    
    // Construtor para inicializar o carro
    public Carro(String modelo, int velocidade) {
        this.modelo = modelo;
        this.velocidade = velocidade;
    }
    
    public String getModelo() {
        return modelo;
    }
    
    public int getVelocidade() {
        return velocidade;
    }
    
    // Constantes para regras de velocidade e multa
    private static final int LIMITE_VELOCIDADE = 120;
    private static final int VALOR_MULTA = 240;
    private static final int ADICIONAL = 20;
    
    // Verifica se o carro ultrapassou o limite e calcula a multa
    public void verificarVelocidade(Carro carro) {
        int velocidade = carro.getVelocidade();
        if (velocidade > LIMITE_VELOCIDADE) {
            int excesso = velocidade - LIMITE_VELOCIDADE;
            int multaAdicional = excesso / 10;
            int valorTotal = VALOR_MULTA + (multaAdicional * ADICIONAL);
            
            System.out.println("O carro " + carro.getModelo() + " foi multado");
            System.out.println("Velocidade: " + velocidade + " km/h");
            System.out.println("Valor da multa: R$" + valorTotal);
        } else {
            System.out.println("O carro " + carro.getModelo() + " está dentro do limite de velocidade");
        }
    }
    
    // Método principal que cria os carros e verifica suas velocidades
    public static void main(String[] args) {
        Carro celta = new Carro("Celta 2010", 120);
        Carro brasilia = new Carro("VW Brasilia 1978", 130);
        Carro uno = new Carro("Uno com Escada", 210);
    
        Carro carro = new Carro("Celta 2010", 120);
        carro.verificarVelocidade(celta);
        carro.verificarVelocidade(brasilia);
        carro.verificarVelocidade(uno);
    }
}
