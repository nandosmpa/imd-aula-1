public class Produto {
    private String nome;
    private double preco;
    private int quantidade;

    public Produto(String nome, double preco, int quantidade) {
        this.nome = nome;
        this.preco = preco;
        this.quantidade = quantidade;
    }

    public void vender(int qtd) {
        if (qtd <= quantidade) {
            quantidade -= qtd;
            System.out.println("Venda realizada com sucesso!");
        } else {
            System.out.println("Estoque insuficiente para a venda!");
        }
    }

    public void reporEstoque(int qtd) {
        if (qtd > 0) {
            quantidade += qtd;
            System.out.println("Estoque reposto com sucesso!");
        } else {
            System.out.println("Quantidade inválida para reposição.");
        }
    }

    public void consultarEstoque() {
        System.out.println("Produto: " + nome);
        System.out.println("Preço: R$ " + preco);
        System.out.println("Quantidade em estoque: " + quantidade);
    }

    // Teste da classe Produto
    public static void main(String[] args) {
        Produto p1 = new Produto("Caderno", 15.90, 50);

        p1.consultarEstoque();
        p1.vender(5);
        p1.consultarEstoque();
        p1.reporEstoque(10);
        p1.
