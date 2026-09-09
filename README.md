# 🛒 Projeto de Planeamento e Execução de Testes — SwagLabs Shopping

Este repositório contém a documentação, o planeamento e as evidências de teste desenvolvidos para a plataforma **SwagLabs Shopping**. O projeto foi realizado como parte do desafio prático de garantia de qualidade (QA) na **Digital Innovation One (DIO)**.

O principal objetivo foi estruturar o fluxo de testes de ponta a ponta (E2E) utilizando metodologias ágeis, técnicas tradicionais e desenvolvimento orientado por comportamento (BDD).

---

## 🗺️ 1. Mind-Map (Mapa Mental)
Para mapear os cenários de teste e garantir a cobertura total das principais funcionalidades da aplicação, foi desenvolvido um mapa mental focado nos seguintes fluxos:
* **Autenticação (Login):** Cenários positivos, negativos e validações de campos obrigatórios.
* **Inventário e Carrinho:** Fluxos de adição e remoção de produtos, com atualização dinâmica do contador.
* **Checkout (Finalização de Compra):** Validação de dados de envio e ecrãs de sucesso.

> 📂 *O ficheiro visual do mapa mental encontra-se anexado na raiz deste repositório.*

---

## 📝 2. User Stories (Histórias de Utilizador)
As regras de negócio e os critérios de aceitação foram documentados com base nas seguintes histórias pensadas para o ecossistema SwagLabs:

### User Story 1: Autenticação com Sucesso
* **Como** um cliente registado na plataforma SwagLabs
* **Quero** inserir o meu utilizador e palavra-passe válidos no formulário de login
* **Para** aceder à loja e visualizar a lista de produtos disponíveis para compra
* **Critérios de Aceitação:**
  1. O sistema deve validar se os campos de texto não estão vazios antes de submeter.
  2. Caso as credenciais existam na base de dados, o utilizador deve ser redirecionado para o catálogo de produtos (`/inventory.html`).

### User Story 2: Adicionar Produto ao Carrinho
* **Como** um utilizador autenticado no sistema
* **Quero** clicar no botão "Add to cart" de um produto do catálogo
* **Para** incluir o artigo no meu carrinho de compras e avançar para o checkout
* **Critérios de Aceitação:**
  1. O texto do botão deve mudar visualmente de "Add to cart" para "Remove".
  2. O contador do ícone do carrinho no topo da página deve incrementar dinamicamente.

---

## 🛠️ 3. Casos de Teste (Jira & Zephyr Scale)
Toda a suíte de testes foi estruturada no Jira através do plugin **Zephyr Scale**, totalizando **6 casos de teste** consolidados e executados no ciclo **`SWAG-R1`**:

| Código | Tipo de Teste | Nome do Caso de Teste | Estado |
| :--- | :--- | :--- | :--- |
| **SWAG-T1** | Step-by-Step | Login com credenciais inválidas exibe mensagem de erro | `PASS` |
| **SWAG-T2** | BDD-Gherkin  | Adicionar produto ao carrinho | `PASS` |
| **SWAG-T3** | BDD-Gherkin  | Login com credenciais inválidas (BDD) | `PASS` |
| **SWAG-T4** | BDD-Gherkin  | Login com credenciais válidas (BDD) | `PASS` |
| **SWAG-T5** | Step-by-Step | Remover produto do carrinho (Tradicional) - Cópia 1 | `PASS` |
| **SWAG-T6** | Step-by-Step | Remover produto do carrinho (Tradicional) - Cópia 2 | `PASS` |

---

## 🐛 4. Plano de Fluxo de Trabalho (Ciclo de Vida do Bug)
Para a gestão eficiente dos defeitos encontrados durante as execuções, foi estabelecido o seguinte fluxo de estados para os bugs dentro do Jira:
1. **Novo (New):** O bug é identificado pelo QA e registado no sistema.
2. **Em Análise (Under Review):** O Product Owner ou equipa técnica avalia a prioridade e o impacto do erro.
3. **Em Correção (In Progress):** O desenvolvedor trabalha na resolução do código.
4. **Pronto para Re-teste (Ready for QA):** A correção é disponibilizada para validação.
5. **Em Re-teste (In QA):** O QA executa novamente os passos para garantir a eficácia da correção.
6. **Fechado (Closed):** O erro foi formalmente mitigado e arquivado com sucesso.

---

## 🎓 Tecnologias e Ferramentas Utilizadas
* **Jira Software:** Gestão ágil do projeto.
* **Zephyr Scale:** Criação, gestão e execução de scripts de teste (Tradicionais e Gherkin).
* **Gherkin / BDD:** Escrita de cenários orientados pelo comportamento humano.
* **GitHub:** Controlo de versão e portefólio de QA.

---
*Desenvolvido com dedicação por [Larissa Ribeiro].*
