Descrição do Modelo de Banco de Dados
O modelo de banco de dados foi projetado para gerenciar o ciclo de vida de pedidos e pagamentos em uma aplicação. Ele inclui tabelas para clientes (Pessoa Física e Pessoa Jurídica), pedidos, produtos e status relacionados. A estrutura foi planejada para garantir a integridade referencial e a organização dos dados.
Principais Tabelas e Relacionamentos

Cliente:
Contém informações gerais de clientes.
É dividida em:
Cliente_PF: Dados específicos de pessoas físicas, como CPF.
Cliente_PJ: Dados específicos de pessoas jurídicas, como CNPJ.


Pedido:
Armazena os dados de pedidos realizados pelos clientes.
Relaciona-se diretamente com:
Cliente: Identifica quem realizou o pedido.
Produto: Os itens incluídos no pedido.
StatusPedido: Indica o andamento do pedido.

Produto:
Contém informações sobre os produtos disponíveis, como código, valor e categoria.

Pagamento:
Gerencia os dados de pagamento associados a pedidos.
Relaciona-se com:
Pedido: Indica o pedido relacionado ao pagamento.
StatusPagamento: Representa o estado do pagamento (aprovado, negado, etc.).

StatusPedido e StatusPagamento:
Representam o estado atual do pedido e do pagamento, respectivamente.
Facilitam o rastreamento do fluxo de trabalho e evitam inconsistências.
