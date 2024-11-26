

---

# MERCADINHO PYTHON

**Autor:** João Geraldo da Silva Neto, FC20230222

Este é um sistema básico de supermercado desenvolvido em Python. Ele gerencia o estoque de produtos, permite adicionar itens ao carrinho de compras, calcula o valor total da compra e realiza a finalização do processo de compra. 

## Funcionalidades

- **Registrar Clientes:** O sistema permite registrar clientes, incluindo nome e CPF.
- **Adicionar Produtos ao Estoque:** Adiciona produtos com nome, preço e quantidade ao estoque.
- **Visualizar Produtos:** Exibe todos os produtos disponíveis no estoque.
- **Adicionar Produtos ao Carrinho:** Os clientes podem adicionar produtos ao carrinho, se houver estoque disponível.
- **Finalizar Compra:** O sistema calcula o total da compra e limpa o carrinho após o pagamento.

## Estrutura do Sistema

### Classes

1. **Produto:** Representa um produto com os atributos de nome, preço e quantidade.
   - Métodos:
     - `atualizar_quantidade`: Atualiza a quantidade de um produto após a venda.
     - `__str__`: Retorna uma representação textual do produto.

2. **Cliente:** Representa um cliente com nome, CPF e um carrinho de compras.
   - Métodos:
     - `adicionar_produto_ao_carrinho`: Adiciona um produto ao carrinho do cliente, verificando se há estoque suficiente.
     - `visualizar_carrinho`: Exibe os produtos no carrinho.
     - `__str__`: Retorna uma representação textual do cliente.

3. **Carrinho:** Representa o carrinho de compras, que pode conter vários produtos.
   - Métodos:
     - `adicionar_produto`: Adiciona um produto ao carrinho.
     - `calcular_total`: Calcula o valor total da compra no carrinho.
     - `__str__`: Exibe os itens do carrinho e o total da compra.

4. **Supermercado:** Gerencia os produtos e clientes do supermercado.
   - Métodos:
     - `adicionar_produto`: Adiciona um produto ao estoque.
     - `buscar_produto`: Pesquisa um produto pelo nome.
     - `registrar_cliente`: Registra um novo cliente.
     - `realizar_venda`: Finaliza a compra de um cliente, exibindo o total da compra.
     - `visualizar_produtos`: Exibe todos os produtos cadastrados no supermercado.

5. **Terminal:** Interface de linha de comando para interação com o sistema.
   - Métodos:
     - Exibe menus e coleta entradas do usuário.

## Fluxo do Programa

1. **Registrar Cliente:** O sistema permite registrar novos clientes, pedindo nome e CPF.
2. **Adicionar Produto ao Estoque:** O sistema permite adicionar novos produtos ao estoque, incluindo nome, preço e quantidade.
3. **Visualizar Produtos:** Exibe todos os produtos disponíveis no estoque.
4. **Adicionar Produto ao Carrinho:** O cliente pode adicionar produtos ao carrinho, desde que haja estoque disponível.
5. **Finalizar Compra:** O cliente pode finalizar a compra, o sistema calcula o total e limpa o carrinho após o pagamento.

## Pontos de Melhoria ou Expansão

- **Validação de Entrada:** A entrada de dados, como preço, quantidade e CPF, não são validadas. Melhorias podem ser feitas para garantir que os dados sejam inseridos corretamente (por exemplo, verificar se o CPF possui 11 dígitos ou se o preço não é negativo).
- **Múltiplos Clientes:** O sistema já suporta múltiplos clientes, mas poderia garantir que um cliente com o mesmo nome não seja registrado mais de uma vez.
- **Recuperação de Carrinho após Fechamento:** O carrinho é limpo após a finalização da compra. Poderia ser interessante manter um histórico de compras.
- **Interface Gráfica:** O sistema está baseado em linha de comando. Uma interface gráfica ou uma aplicação web poderia ser desenvolvida para melhorar a interação com o usuário.
- **Controle de Estoque:** O estoque poderia ser verificado antes de finalizar a venda, para garantir que o produto esteja disponível no momento do pagamento.

## Exemplo de Execução

Suponha que você execute o sistema e realize as seguintes operações:

1. **Registrar Cliente:**
   - Cliente João Silva é registrado.

2. **Adicionar Produto:**
   - Produto "Arroz" com preço R$ 10,00 e 50 unidades é adicionado ao estoque.

3. **Adicionar Produto ao Carrinho:**
   - João adiciona 3 unidades de "Arroz" ao seu carrinho.

4. **Finalizar Compra:**
   - João finaliza a compra, e o sistema calcula o total (R$ 30,00).
