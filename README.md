# jvi-investimentos---projeto-excel-investimentos

# Simulador de Investimentos em Fundos Imobiliários (FII) - Excel

> **Projeto desenvolvido para o desafio da DIO:** Construção de uma ferramenta prática de simulação de investimentos em Fundos Imobiliários utilizando Excel.

## Sobre o Projeto

Este projeto consiste em uma planilha inteligente desenvolvida para automatizar cálculos essenciais na tomada de decisão de investimentos em FIIs (Fundos de Investimento Imobiliário). 

O diferencial da ferramenta é a **personalização dinâmica de carteira**: o usuário define seu perfil de investidor e o montante mensal, e a planilha calcula automaticamente a alocação ideal de ativos baseada em premissas pré-definidas.

---

## Funcionalidades Principais

A ferramenta permite simular e visualizar:

* **Perfil de Investidor Dinâmico:** Seleção via menu suspenso (Conservador, Moderado, Agressivo) que altera automaticamente a estratégia de alocação.
* **Distribuição de Ativos:** Divisão automática do aporte entre diferentes tipos de FIIs (Papel, Tijolo, Híbridos, FOFs, Desenvolvimento, Hotelarias).
* **Projeção de Patrimônio:** Cálculo do valor acumulado ao longo do tempo.
* **ROI (Retorno sobre Investimento):** Comparativo entre valor desembolsado e valor bruto final.

---

## ⚙️ Estrutura e Lógica (Como funciona)

O projeto foi dividido em duas abas principais para manter a organização e auditabilidade:

### 1. Aba 'Inputs - Apoio' (Database)
Funciona como o "motor" de regras da planilha. Contém a matriz de alocação de ativos baseada no risco.
* **Coluna Chave:** Uma coluna auxiliar criada para gerar identificadores únicos (Ex: 'Agressivo-PAPEL', 'Moderado-TIJOLO').
* **Matriz de Porcentagem:** Define quanto de cada aporte vai para cada setor dependendo do perfil escolhido.

### 2. Aba 'Investimento' (Dashboard)
A interface onde o usuário interage.
* **Automação com PROCV (VLOOKUP):** Utilizada para ler a escolha do usuário no menu suspenso, cruzar com a aba de apoio e retornar a porcentagem correta de alocação sem necessidade de macros complexas.
* **Formatação Condicional:** Para facilitar a leitura visual dos dados.
* **Validação de Dados:** Menus suspensos para evitar erros de digitação nos perfis.

---

## Tecnologias e Fórmulas Utilizadas

* **Microsoft Excel** (Compatível com Office 365/2019+)
* **Principais Funções:**
    * `PROCV` (VLOOKUP): Para busca dinâmica de perfis.
    * `CONCATENAR` (ou `&`): Para criação de chaves primárias compostas.
    * `SE` (IF): Para tratativa de erros e lógica condicional.
    * `SOMA` (SUM) e Operações Financeiras básicas.

---

## Como Usar

1. Baixe o arquivo `.xlsx`.
2. Em seus dados, insira os valores correspondentes em cada campo para entender em quanto tempo consegue a construção do seu patrimônio 
3. Na parte de 'patrimônio' é possível ver também o rendimento nos anos que tiver interesse, assim como seus dividendos
4. No campo de 'estratégias de investimentos', localize **Perfil** e selecione sua estratégia (ex: *Agressivo*) para ter uma noção de como cada perfil consegue alcançar sua meta
5. Em diversificação da carteira, selecione o **Perfil** e insira o **Valor a investir por mês** (ex: R$ 1.000,00).
6. Observe a tabela "Diversificação da Carteira" se atualizar automaticamente com os valores sugeridos para cada tipo de FII.

---

## Autora

**Jéssica Migliorati da Silva** Estudante de Administração 

[https://www.linkedin.com/in/j%C3%A9ssica-migliorati-844439103/]

---

## 📝 Licença
>
> Sinta-se à vontade para contribuir com melhorias, como gráficos,
> dashboard ou novos cenários de simulação.
