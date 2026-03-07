# Teste Técnico – QA Tester - Processo Seletivo – 4blue

# Relatário e testes exploratórios
Este repositório contém relatório de testes exploratórios realizados no sistema:
https://qa-play-sim.lovable.app/

O objetivo da analise foi identificar falhas funcionais, inconsistências de experiência do usuário e possíveis problemas de segurança nas seguintes telas:
- Tela de Login
- Tela de Criação de Conta
- Tela de sucesso

---

# Objetivo da Avaliação
Durante a análise foram avaliados os seguintes aspectos:
- Validação de campos
- Fluxos de autenticação
- Consistência de navegação
- Tratamento de erros
- Regras básicas de negócio
- Possíveis vulnetabilidades de segurança

---

# Estratégia de Testes
Foi utilizada a técnica de **Testes Exploratórios**.

## Abordagem incluiu:
- Testes de campos obrigatórios
- Testes de dados inválidos
- Testes de consistência de fluxo
- Testes de autenticação
- Testes de duplicidade de cadastro
- Testes de comportamento inesperado do sistema

---

# Ambiente de Testes

| Item | Detalhes |
| ---- | -------- |
| Sistema |  4Blue QA Play |
| URL | https://qa-play-sim.lovable.app |
| Navegador | Firefox - 148.0 (64-bits) / Chrome - 145.0.7632.160 (Versão oficial) 64 bits |
| Sistema Operacional | Windows 11 |

---

# Bugs Identificados
Durante os testes exploratórios foram identificados os seguintes defeitos no sistema.

## Título:

BUG- → Sistema permite cadastro com campos obrigatórios vazios

## Descrição:
O sistema permite a criação de contas mesmo quando nenhum campo do formulário de cadastro é preenchido.

## Passos para reproduzir
    1. Acessar página de cadastro
    2. Não preencher nenhum campo
    3. Clicar no botão "Cadastrar"

## Resultado atual:
O sistema redireciona para "/sucesso?op=cadastro", exibindo mensagem "Conta criada com sucesso"

## Resultado esperado:
O resultado deveria impedir o envio do formulário e exibir mensagem informando "Os campos obrigatórios devem ser preenchidos".

## Severidade
Crítico

## Prioridade
Alta

## Evidências
![Evidência do Bug](evidencias/1-cadastro_campos_vazios.gif)