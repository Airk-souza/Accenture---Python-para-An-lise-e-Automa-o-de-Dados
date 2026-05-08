# 🐍 Miniguia de Estudos: Python para Iniciantes em Análise de Dados - Dominando Ambientes e Dependências

Este repositório contém o Desafio de Projeto da DIO, desenvolvido como parte do bootcamp **Accenture - Python para Análise e Automação de Dados**. 

Neste projeto, utilizei o NotebookLM (Inteligência Artificial) como uma ferramenta de aprendizagem ativa para explorar e documentar a base fundamental de qualquer projeto de dados em Python: a configuração de ambientes de desenvolvimento e o gerenciamento de bibliotecas.

## 🎯 Contexto e Objetivos

**Tema Escolhido:** Configuração de Ambientes Virtuais e Gerenciamento de Dependências para Análise de Dados em Python.

**Por que este tema?**
Muitos iniciantes em análise de dados pulam direto para o Pandas ou Scikit-learn e acabam sofrendo com o famoso erro "na minha máquina funciona" ou conflitos de versão. O objetivo deste caderno temático é desmistificar o uso de ambientes virtuais (venv, Conda) e gerenciadores de pacotes (pip, poetry, requirements.txt), garantindo que qualquer projeto de análise de dados seja reprodutível, organizado e profissional desde o dia zero.

**Objetivos de Estudo:**
1. Entender o que é e por que usar um ambiente virtual em projetos de dados.
2. Comparar ferramentas nativas (`venv`) com soluções de mercado (`Conda`, `Poetry`).
3. Compreender a importância do arquivo `requirements.txt`.
4. Mapear o processo de instalação de bibliotecas essenciais de dados (Pandas, Scikit-learn).

---

## 📚 Curadoria de Fontes

Para alimentar o NotebookLM e criar uma base de conhecimento sólida, selecionei os seguintes artigos, documentações e tutoriais (disponíveis abertamente na internet e em comunidades de desenvolvedores):

1. **Guia Completo para Usar o Virtual Environment (venv) no Python** - *DEV Community* (Artigo detalhando a ferramenta nativa do Python).
2. **Detailed Guide: Virtualenv vs Conda** - *DEV Community* (Comparativo essencial para cientistas de dados).
3. **Uso do requirements.txt em Projetos Python** - *Python Floripa* (Boas práticas de reprodutibilidade).
4. **Como resolver dependências no Python com Poetry** - *Academify* (Visão sobre ferramentas modernas de gerenciamento).
5. **User Guide — pandas 3.0.2 documentation & scikit-learn docs** (Documentação oficial das principais bibliotecas de análise de dados).

---

## 🤖 Engenharia de Prompts e "Cicatrizes"

Para extrair o melhor do NotebookLM, utilizei uma abordagem iterativa. Abaixo documento o meu processo de raciocínio, os testes e os ajustes (troubleshooting).

### Interação 1: Entendendo o básico
* **Prompt Testado:** *"O que é um ambiente virtual e por que eu preciso disso para analisar dados?"*
* **Resultado:** A IA deu uma resposta boa, mas muito focada em desenvolvimento web genérico.
* **Troubleshooting (A "Cicatriz"):** Percebi que precisava dar contexto de "Análise de Dados" e focar nas bibliotecas gigantes (como pandas/scikit-learn) que costumam causar conflitos.
* **Prompt Refinado:** *"Com base nos documentos fornecidos, explique o conceito de ambiente virtual focando especificamente nas dores de um analista de dados que trabalha com Pandas e Scikit-learn. Qual problema o `venv` resolve nesse cenário?"*
* **Resultado Obtido:** Excelente. A IA explicou que isolar projetos evita que a atualização do Pandas para um projeto quebre o código de um projeto antigo que dependia de uma versão anterior.

### Interação 2: Conda vs Venv
* **Prompt Testado:** *"Qual a diferença entre venv e Conda?"*
* **Troubleshooting:** A resposta foi muito técnica, listando comandos do terminal. Faltou foco estratégico.
* **Prompt Refinado:** *"Aja como um Engenheiro de Dados Sênior orientando um Cientista de Dados Júnior. Use o documento 'Virtualenv vs Conda' para montar uma tabela comparativa simples dizendo quando eu devo escolher o 'venv' e quando devo escolher o 'Conda' para um projeto de Machine Learning."*

---

## 📖 Miniguia de Estudo: Ambientes em Python

Abaixo apresento o conhecimento consolidado através do estudo com a IA.

### 📝 Resumo Estruturado do Assunto

**1. O Problema da Instalação Global:**
Instalar bibliotecas (como Pandas ou Scikit-learn) globalmente no seu computador é um erro. Se o Projeto A precisa do Pandas 1.0 e o Projeto B precisa do Pandas 2.0, haverá conflito.

**2. A Solução: Ambientes Virtuais:**
* **`venv`:** Vem embutido no Python. É leve e cria uma pasta isolada para o projeto. Ótimo para projetos simples.
* **`Conda`:** Muito popular em Ciência de Dados. Além de pacotes Python, ele instala dependências externas (em C/C++) que muitas bibliotecas matemáticas exigem.
* **`Poetry`:** Uma ferramenta moderna que não só gerencia o ambiente virtual, mas também resolve conflitos de dependências de forma inteligente, substituindo o tradicional `pip`.

**3. Reprodutibilidade:**
Para que outra pessoa (ou você no futuro) rode seu código, você precisa exportar as dependências. O arquivo padrão para isso é o `requirements.txt`, gerado pelo comando `pip freeze > requirements.txt`.

### 🔤 Glossário

* **Ambiente Virtual:** Um diretório isolado que contém sua própria instalação do Python e suas próprias bibliotecas.
* **Dependência:** Um pacote ou biblioteca de terceiros (ex: Pandas) que o seu código precisa para funcionar.
* **requirements.txt:** Arquivo de texto que lista todas as bibliotecas e suas exatas versões utilizadas em um projeto.
* **Ativação (Activate):** Comando executado no terminal (`source venv/bin/activate` no Mac/Linux ou `venv\Scripts\activate` no Windows) que diz ao sistema operacional para usar o Python do ambiente virtual, e não o global.
* **Pandas / Scikit-learn:** Bibliotecas de alta performance para manipulação de dados e machine learning, respectivamente, que exigem rigoroso controle de versão.

### 🔄 Prompts Reutilizáveis (Para futuras revisões)

Guarde estes prompts para usar no NotebookLM ou ChatGPT sempre que precisar relembrar o assunto:

1. *"Quero iniciar um novo projeto de análise de dados. Gere o passo a passo de comandos no terminal para criar um ambiente virtual (venv), ativá-lo, instalar pandas e scikit-learn, e gerar o arquivo requirements.txt."*
2. *"Estou recebendo um erro de 'ModuleNotFoundError' no meu VS Code, mas já instalei a biblioteca. Com base nos meus estudos sobre ambientes virtuais, quais são os 3 passos para investigar se o meu VS Code está usando o interpretador correto?"*
3. *"Explique de forma simples como migrar um projeto que usa `requirements.txt` padrão para o `Poetry`."*

---
*Projeto desenvolvido para o bootcamp **Accenture - Python para Análise e Automação de Dados** na plataforma [DIO](https://www.dio.me/).*
