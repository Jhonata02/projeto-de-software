
## Atividade 2 - Padrões GRASP

Considerando os padrões GRASP (information expert, creator, low coupling e high cohesion), desenvolva um código em Java (não deve ser web) para um mercado que permita a venda de produtos a partir de um pagamento. Os valores dos itens a serem comprados dependem da quantidade de produtos de cada item. Itens com 100 ou mais produtos recebem um desconto de 10% em seu preço. Explique e justifique o uso de cada um dos padrões GRASP em seu código na folha com a modelagem UML. 

## Resposta

Aplicação dos Padrões GRASP:

Information Expert:

A lógica para calcular o valor com desconto está na classe ItemVenda, que é a mais adequada para deter essas informações, já que ela conhece o preço do produto e a quantidade. O padrão garante que a responsabilidade de processamento esteja com o objeto que possui as informações necessárias.

Creator:

A classe Venda é responsável por criar e manter a lista de itens de venda. Como a venda "utiliza" os itens diretamente, faz sentido que ela seja a criadora deles. Essa abordagem simplifica o design e promove coesão.

Low Coupling:

As classes estão acopladas minimamente. Por exemplo, ItemVenda depende de Produto, mas Venda apenas conhece a lista de itens, sem detalhes sobre os produtos. Isso facilita manutenção e alterações futuras.

High Cohesion:

Cada classe tem uma única responsabilidade bem definida:
Produto mantém informações sobre o produto.
ItemVenda calcula o valor total considerando a quantidade e possíveis descontos.
Venda gerencia os itens e calcula o total da venda.
Essa divisão clara de responsabilidades promove coesão alta.
