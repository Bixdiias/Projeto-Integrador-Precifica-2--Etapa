# Precifica — Ferramenta de Precificação e Propostas Comerciais

Aplicação web responsiva desenvolvida para auxiliar profissionais autônomos, freelancers e prestadores de serviços no cálculo do valor da hora de trabalho, elaboração de orçamentos, simulação de cenários comerciais e geração de propostas prontas para exportação em PDF.

> **Projeto Integrador — Boas Práticas de Desenvolvimento de Software**  
> Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas (ADS) — Centro Universitário Senac EAD

---

## 🎯 Problema Resolvido

Profissionais autônomos frequentemente enfrentam dificuldades para precificar seus serviços de forma justa e lucrativa, por não considerarem seus custos fixos mensais, a capacidade real de horas produtivas e a margem de lucro desejada. O **Precifica** centraliza todo esse fluxo em uma única interface intuitiva, eliminando a necessidade de múltiplas planilhas e editores externos.

---

## ✨ Funcionalidades Principais

* **Visão Geral (Dashboard):** Painel inicial com acompanhamento em tempo real da quantidade de orçamentos cadastrados, soma total dos valores orçados e valor/hora de referência.
* **Cálculo do Valor da Hora:** Definição automática do custo operacional por hora e do valor recomendado com base nos custos fixos mensais, dias trabalhados, horas produtivas por dia e margem de lucro desejada.
* **Montagem de Orçamento:** Cadastro do projeto e cliente, descrição do escopo, adição dinâmica de etapas com horas estimadas e inclusão de custos adicionais/terceiros.
* **Comparação de Cenários Comerciais:** Simulação interativa entre pagamento **À Vista** (com desconto configurável apenas sobre as horas técnicas), **Padrão (50% + 50%)** e **Parcelado (3x)**, exibindo alertas visuais de margem líquida real.
* **Proposta Comercial & Exportação PDF:** Documento consolidado com os dados do profissional (com seleção exclusiva e máscara automática para **CPF** de até 11 dígitos ou **CNPJ** de até 14 dígitos), etapas, condições de pagamento e exportação limpa via `@media print`.
* **Histórico Local (`localStorage`):** Persistência automática dos dados no navegador, permitindo salvar, editar, visualizar propostas anteriores ou excluir orçamentos sem necessidade de servidor externo.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estruturação semântica das telas e do documento de proposta.
* **CSS3:** Estilização responsiva (*Flexbox*, *CSS Grid*, variáveis CSS) e regras dedicadas de impressão (`@media print`) para geração de PDF.
* **JavaScript (ES6+):** Manipulação do DOM, regras de negócio financeiras, formatação monetária (`Intl.NumberFormat` em BRL), máscaras de validação (CPF/CNPJ) e persistência via `localStorage`.

---

## 📁 Estrutura de Pastas

```text
Precifica P.I - 2ª Etapa/
├── css/
│   └── style.css              # Estilos do painel, responsividade e layout PDF
├── javascript/
│   └── funcionalidades.js     # Lógica de cálculo, navegação, máscaras e localStorage
├── index.html                 # Estrutura principal da aplicação (SPA)
└── README.md                  # Documentação do projeto