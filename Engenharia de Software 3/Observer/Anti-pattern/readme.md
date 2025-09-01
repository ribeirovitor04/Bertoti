<img width="477" height="763" alt="479005327-7c472de2-01c4-4906-9f76-3976c2d66129" src="https://github.com/user-attachments/assets/479dfa18-661b-41b9-af9c-2b97716afb48" />

```bash
// Observer
interface Licitante {
    void atualizar(String nomeProduto, double novoLance);
}
```

```bash
// Subject
interface ProdutoLeilao {
    void registrarLicitante(Licitante licitante);
    void removerLicitante(Licitante licitante);
    void notificarLicitantes();
}
```

```bash
import java.util.ArrayList;
import java.util.List;

// ConcreteSubject
class Produto implements ProdutoLeilao {
    private String nome;
    private double lanceAtual;
    private List<Licitante> licitantes = new ArrayList<>();

public Produto(String nome, double lanceInicial) {
    this.nome = nome;
    this.lanceAtual = lanceInicial;
}

public void novoLance(double valor) {
    this.lanceAtual = valor;
    notificarLicitantes();
}

@Override
public void registrarLicitante(Licitante licitante) {
    licitantes.add(licitante);
}

@Override
public void removerLicitante(Licitante licitante) {
    licitantes.remove(licitante);
}

@Override
public void notificarLicitantes() {
    for (Licitante licitante : licitantes) {
        licitante.atualizar(nome, lanceAtual);
    }
  }
}
```

```bash
// ConcreteObserver
class LicitanteConcreto implements Licitante {
private String nome;

public LicitanteConcreto(String nome) {
    this.nome = nome;
}

@Override
public void atualizar(String nomeProduto, double novoLance) {
    System.out.println(nome + ", o produto " + nomeProduto + " recebeu um novo lance de R$ " + novoLance);
  }
}
```

```bash
public class Leilao {
    public static void main(String[] args) {
        Produto produto = new Produto("Notebook Gamer", 2500.00);

        Licitante licitante1 = new LicitanteConcreto("João");
        Licitante licitante2 = new LicitanteConcreto("Maria");

        produto.registrarLicitante(licitante1);
        produto.registrarLicitante(licitante2);

        produto.novoLance(2600.00);

        produto.removerLicitante(licitante1);

        produto.novoLance(2700.00);
    }
}
```
