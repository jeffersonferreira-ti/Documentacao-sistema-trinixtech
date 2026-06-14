# TrinixTech - Sistema de Gestão para Assistência Técnica

Repositório de documentação do **TrinixTech**, um sistema web desenvolvido para apoiar a gestão de uma loja de assistência técnica de eletrônicos. A solução centraliza o controle de clientes, ordens de serviço, vendas e estoque, facilitando o acompanhamento das operações e a tomada de decisões.

O projeto foi desenvolvido como parte do **Projeto Interdisciplinar - AAP 4**, do curso de **Gestão da Tecnologia da Informação da Fatec Barueri**, em 2026.

> Este repositório reúne a documentação acadêmica e técnica, os requisitos, diagramas, modelos de banco de dados, protótipos e registros visuais do sistema. O código-fonte da aplicação não está armazenado neste repositório.

## Objetivo

O TrinixTech tem como objetivo digitalizar e organizar os processos administrativos de uma assistência técnica, reunindo informações importantes em uma única plataforma. O sistema busca reduzir controles manuais, evitar a perda de dados e tornar mais eficientes as atividades de atendimento, manutenção, estoque e vendas.

## Funcionalidades

### Dashboard

- Indicadores de ordens de serviço em aberto;
- Total de vendas realizadas no mês;
- Quantidade de itens em estoque;
- Alertas de estoque crítico;
- Exibição de ordens de serviço recentes.

### Clientes

- Cadastro de clientes;
- Consulta e edição de dados;
- Exclusão de registros;
- Armazenamento de nome, telefone e e-mail.

### Ordens de Serviço

- Abertura e acompanhamento de ordens de serviço;
- Registro do dispositivo e do problema relatado;
- Associação da ordem a um cliente;
- Controle de valor e status do atendimento;
- Atualização do andamento do serviço.

### Estoque

- Cadastro de peças e acessórios;
- Registro de SKU, preço e quantidade;
- Edição e exclusão de produtos;
- Identificação de itens com baixo estoque;
- Baixa automática de itens após uma venda.

### Vendas

- Registro de vendas;
- Associação da venda a um cliente;
- Seleção de produtos e quantidades;
- Registro da forma de pagamento;
- Cálculo do valor total;
- Consulta de vendas por mês;
- Indicadores de faturamento, quantidade de vendas e ticket médio.

### Autenticação e Segurança

- Cadastro e login por e-mail e senha;
- Autenticação gerenciada pelo Supabase Auth;
- Sessões identificadas por tokens JWT;
- Isolamento dos dados de cada usuário;
- Políticas de acesso com Row Level Security (RLS).

## Tecnologias

### Front-end

- **React** - construção da interface;
- **TypeScript** - tipagem estática e maior segurança no desenvolvimento;
- **Tailwind CSS** - estilização e responsividade;
- **Lovable** - apoio na geração e organização dos componentes.

### Back-end

- **Supabase** - plataforma de back-end como serviço;
- **PostgreSQL** - banco de dados relacional;
- **Supabase Auth** - autenticação de usuários;
- **Row Level Security** - controle de acesso aos registros;
- **supabase-js** - integração entre front-end e back-end;
- **API REST e Realtime** - acesso e atualização dos dados.

## Arquitetura e Banco de Dados

O front-end consome os serviços fornecidos pelo Supabase por meio da biblioteca `supabase-js`. A autenticação é integrada às requisições, e as políticas de RLS garantem que cada conta acesse somente os próprios registros.

O modelo de dados implementado possui cinco tabelas principais:

| Tabela | Responsabilidade |
| --- | --- |
| `clientes` | Armazena os dados dos clientes |
| `ordens_servico` | Registra e acompanha os serviços técnicos |
| `estoque` | Controla peças e acessórios disponíveis |
| `vendas` | Armazena as transações realizadas |
| `itens_venda` | Relaciona os produtos e as quantidades de cada venda |

## Interface

A aplicação utiliza uma interface responsiva em tema escuro, com menu lateral e componentes padronizados. O design prioriza contraste, legibilidade, navegação rápida e organização visual das informações.

### Landing page

![Tela inicial da landing page](<./Design Home landing page.png>)

### Sistema de gestão

![Tela inicial do sistema de gestão](<./Layout home sistema de controle de estoque e vendas.png>)

## Documentação Disponível

Os principais artefatos deste repositório incluem:

- [Documentação final do projeto](<./Documentação_Final_TrinixTech.pdf>);
- [Escopo do projeto](<./Escopo_-_Squad_212.pdf>);
- [Requisitos funcionais e não funcionais](<./Requisitos_AAP4.pdf>);
- [Documentação de front-end](<./TrinixTech_Front-End.docx>);
- [Documentação de back-end](<./TrinixTech_BackEnd.docx>);
- Diagramas UML de caso de uso, classes, atividades, sequência, objetos, componentes, colaboração, implantação e estados;
- Modelos conceitual e lógico do banco de dados;
- Protótipos da landing page e das telas do sistema;
- Registros visuais de funcionalidades e trechos de implementação.

## Estrutura do Repositório

```text
.
|-- Documentação_Final_TrinixTech.pdf
|-- Escopo_-_Squad_212.pdf
|-- Requisitos_AAP4.pdf
|-- TrinixTech_Front-End.docx
|-- TrinixTech_BackEnd.docx
|-- Diagrama de Classes.png
|-- Diagrama de sequência.png
|-- Layout ...
|-- Design ...
`-- demais documentos e evidências do projeto
```

## Escopo e Limitações

O projeto concentra-se nas funcionalidades essenciais para a gestão da assistência técnica. Integrações mais complexas, como gateways de pagamento, emissão fiscal, notificações externas e aplicativo móvel, não fazem parte da versão atual.

Os requisitos levantados representam a visão completa do produto. Parte deles foi definida para evolução futura e não está necessariamente implementada no protótipo atual.

## Melhorias Futuras

- Exportação de relatórios em PDF;
- Aplicativo móvel integrado;
- Notificações automáticas sobre o status das ordens de serviço;
- Funções e gatilhos no PostgreSQL para regras de negócio;
- Rotinas de backup automatizadas;
- Integração com meios de pagamento e emissão fiscal;
- Perfis de acesso e trilha de auditoria mais detalhados.

## Equipe

- Gabriel de Souza;
- Igor Akitomi;
- Jefferson Ferreira;
- Leonardo de Novaes;
- Renan Macorin;
- Vinicius da Silva.

**Orientação:** Prof. Vander Ribeiro Elme  
**Instituição:** Fatec Barueri - Padre Danilo José de Oliveira Ohl  
**Curso:** Gestão da Tecnologia da Informação  
**Ano:** 2026

## Finalidade Acadêmica

O desenvolvimento do TrinixTech permitiu aplicar conhecimentos de levantamento de requisitos, análise de sistemas, modelagem UML, banco de dados, desenvolvimento web, segurança e documentação de software em uma solução voltada a um problema real de gestão empresarial.
