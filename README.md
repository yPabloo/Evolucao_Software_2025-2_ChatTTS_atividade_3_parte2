# Otimização da Esteira de CI/CD – ChatTTS

Este repositório apresenta uma **intervenção técnica pontual** realizada sobre a infraestrutura de **CI/CD** do projeto open-source **ChatTTS**, como parte da Atividade 3 (Parte 2) da disciplina **Evolução de Software**.

O objetivo da intervenção foi **otimizar a esteira de automação existente**, reduzindo o tempo de feedback do pipeline e diminuindo a barreira de entrada para novos contribuidores, com base no diagnóstico realizado na Parte 1 da atividade.

---

## 📌 Contexto

Na análise inicial (Atividade 3 – Parte 1), o projeto ChatTTS foi classificado no **Cenário A**, pois já possuía CI/CD implementado via **GitHub Actions**.  
Entretanto, foram identificados pontos de melhoria relacionados a:

- Tempo de execução do pipeline
- Clareza para execução local de testes
- Onboarding de novos contribuidores

Este repositório contém as melhorias implementadas para tratar esses pontos.

---

## 🔧 Alterações Realizadas

### 1. Otimização do Pipeline de Testes

- Manutenção do workflow original:  
  `.github/workflows/unitest.yml` (versão anterior)

- Criação de uma nova versão otimizada do workflow:  
  `.github/workflows/unitest.yml` (nova versão)

#### Melhorias aplicadas:
- Adição de **cache de dependências** utilizando `actions/cache`
- Redução do tempo de instalação de pacotes
- Pipeline mais rápido e com feedback mais ágil

---

### 2. Atualização do `requirements.txt`

- Revisão e organização das dependências do projeto
- Facilita:
  - Reprodutibilidade do ambiente
  - Execução local dos testes
  - Consistência entre ambiente local e CI

---

### 3. Documentação para Contribuidores

- Adição do arquivo **`CONTRIBUTING.md`**, contendo:
  - Pré-requisitos do ambiente
  - Instalação de dependências
  - Execução dos testes localmente
  - Boas práticas antes de abrir um Pull Request
  - Relação entre validações locais e pipeline de CI

Essa documentação reduz a barreira de entrada e torna o processo de contribuição mais previsível.

---

## 📂 Estrutura Relevante do Repositório

```text

old workflow/
     └── unitest.yml        # Workflow original
new workflow/
     └── unitest.yml        # Workflow otimizado (nova versão)
requirements.txt            # Dependências atualizadas
CONTRIBUTING.md             # Guia para novos contribuidores

```
---

**Equipe:**  
DOUGLAS DE OLIVEIRA DEDA  
GABRIEL DOS SANTOS ALMEIDA  
HENRICK CARDOSO DOS SANTOS  
IAN DA SILVA SANTOS CONCEIÇÃO  
MARIANA SOUZA NUNES  
PABLO ALVES FREIRE  
RAFAEL LAUTON SANTOS DE OLIVEIRA  
YASMIM DE ANDRADE LIMA  

**Disciplina:** Evolução de Software 2025-2
