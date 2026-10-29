
# 🏢 Auditoria de Orçamentos Corporativos (Python)

[![Python Version](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)](https://github.com/chagasmatheus1211/portfolio-matheus-chagas-mauriz-coque/blob/main/Sistemas_de_auditoria_de_recursos_corporativos)

## 📖 Sobre o Projeto

Este projeto foi desenvolvido como parte da disciplina de Engenharia de Software. O objetivo do script é processar e calcular o orçamento de uma estrutura organizacional complexa, representada por dicionários aninhados de uma multinacional, aplicando regras de negócio dinâmicas e auditoria de execução.

A solução utiliza conceitos de Python para garantir flexibilidade, organização e rastreabilidade.

## 🚀 Funcionalidades

- 📊 **Cálculo Hierárquico:** varredura completa da estrutura corporativa, independentemente do nível de profundidade.
- 🔍 **Filtros Dinâmicos:** capacidade de ignorar setores específicos e todos os seus subsetores durante o cálculo financeiro.
- 💱 **Conversão de Câmbio:** suporte a parâmetros opcionais para conversão de moedas durante a execução.
- 🕵️ **Sistema de Auditoria:** monitoramento automatizado do tempo de execução e registro (*logging*) dos parâmetros utilizados na operação financeira.

## 🛠️ Tecnologias e Conceitos Aplicados

- 🐍 **Python:** linguagem utilizada no desenvolvimento.
- 🔄 **Funções Recursivas:** navegação pela estrutura hierárquica de dicionários aninhados.
- 🧩 **Decorators:** implementação do `@auditor` para adicionar registros e cronometragem sem modificar a lógica principal.
- 📦 **`*args` e `**kwargs`:** passagem dinâmica de argumentos, departamentos a ignorar e taxas de câmbio.
- ⏱️ **Biblioteca `time`:** medição do tempo de execução.

## ⚙️ Como Executar

### 📋 Pré-requisitos

- Python 3.8 ou superior instalado.
- Terminal, prompt de comando ou ambiente de desenvolvimento Python.

### ▶️ Passo a Passo

**1. Clone o repositório**

```bash
git clone https://github.com/Lusca2803/projeto-sistema-de-auditoria-de-recursos-corporativos.git
```

**2. Acesse a pasta do projeto**

```bash
cd projeto-sistema-de-auditoria-de-recursos-corporativos
```

**3. Execute o script principal**

```bash
python main.py
```

## 🧠 Lógica e Estrutura do Código

### 🔄 Recursão e Hierarquia Organizacional

A estrutura da empresa foi representada como uma árvore de departamentos. Cada chave do dicionário pode conter outro dicionário, representando subdepartamentos, ou um valor numérico correspondente ao orçamento.

A função percorre cada item verificando o tipo do valor. Se encontrar outro dicionário, chama a si mesma para continuar percorrendo a hierarquia. Se encontrar um número, soma esse valor ao total.

Dessa forma, o algoritmo pode trabalhar com diferentes níveis organizacionais sem precisar conhecer antecipadamente a profundidade da estrutura.

### ⏱️ Decorator de Auditoria

O decorator foi implementado para adicionar uma camada de auditoria sem alterar a lógica principal da função de cálculo.

Uma função intermediária (*wrapper*) intercepta a execução da função original, registra os argumentos recebidos e mede o tempo de processamento utilizando a biblioteca `time`.

O uso de `*args` e `**kwargs` permite que o decorator receba diferentes argumentos, tornando a implementação mais flexível e reutilizável.

### 🗂️ Organização dos Dados

Os dados simulados representam uma empresa por meio de dicionários aninhados. Cada chave principal identifica um setor ou unidade, como `Matriz` e `Filial_SP`.

Dentro dessas unidades existem departamentos e subdepartamentos, formando uma estrutura hierárquica. Os níveis finais armazenam valores numéricos que representam os orçamentos de cada área.

Essa organização facilita a aplicação da recursão e permite representar empresas com diferentes quantidades de departamentos e níveis organizacionais.

## 📂 Estrutura do Projeto

```text
Sistemas_de_auditoria_de_recursos_corporativos/
├── README.md
└── main.py
```

- 📘 `README.md`: documentação e apresentação do projeto.
- 🐍 `main.py`: código-fonte do sistema de auditoria de orçamentos.

## 💻 Acesse o Projeto

🐍 **[Visualizar código-fonte (main.py)](main.py)**

📁 **[Acessar repositório do projeto no GitHub](https://github.com/Lusca2803/projeto-sistema-de-auditoria-de-recursos-corporativos)**

## 👤 Autor

**Matheus Chagas Mauriz Coque**

🎓 Estudante de Engenharia de Software

- 💼 [LinkedIn](https://www.linkedin.com/in/matheus-chagas-coque-b190ba39b/)
- 🐙 [GitHub](https://github.com/chagasmatheus1211)
- 📧 [E-mail](mailto:chagasmatheus1211@gmail.com)

---

⭐ *Projeto acadêmico com foco na aplicação prática de conceitos da linguagem Python, recursão e auditoria de execução.*

⬅️ **[Voltar ao portfólio principal](https://github.com/chagasmatheus1211/portfolio-matheus-chagas-mauriz-coque/tree/main)**
