# PSE em Ação — Sistema de Apoio à Vacinação Escolar

Sistema em linguagem C, executado em terminal, para apoiar o planejamento, registro e acompanhamento de ações escolares realizadas no âmbito do **Programa Saúde na Escola (PSE)**.

Atividade Extensionista Prática (AEP) — 2º Semestre de 2026
Curso: 

## Integrantes

Arthur da Silva Mota – RA 26002999-2 

João Fábio Pires Parra – RA 26006728-2 

Lucas Masaki Sversuti – RA 26002032-2 


## Descrição do projeto

O Programa Saúde na Escola (PSE) inclui, entre suas ações prioritárias, a verificação da situação de ações. Apesar dos avanços recentes na integração entre saúde e educação, a execução dessas ações ainda enfrenta desafios de comunicação, planejamento e acompanhamento, muitas vezes registradas em anotações e planilhas dispersas.

Este projeto propõe uma aplicação simples em C, executada em terminal, capaz de:

- Cadastrar ações (código, escola, tema, data prevista, público-alvo, responsável, quantidade prevista);
- Listar e pesquisar ações por código, escola ou tema;
- Atualizar a situação de uma ação (planejada, realizada ou cancelada) e registrar a quantidade efetiva de participantes;
- Gerar um resumo geral com quantidade de ações por situação e percentual de participação.

O sistema **não coleta nem armazena dados clínicos individuais** de estudantes (nome, diagnóstico, prontuário), trabalhando apenas com informações coletivas e fictícias sobre as ações planejadas, sem substituir o trabalho de profissionais de saúde.

### Requisitos funcionais (resumo)

| Código | Descrição |
|---|---|
| RF01 | Cadastro de ação |
| RF02 | Listagem de todas as ações cadastradas |
| RF03 | Pesquisa de ações por código, escola ou tema |
| RF04 | Atualização da situação da ação e registro de participantes efetivos |
| RF05 | Geração de resumo geral (ações e percentual de participação) |
| RF06 | Validação de entradas (códigos duplicados, campos vazios, valores inválidos) |

### Requisitos não funcionais (resumo)

- Execução em terminal, sem interface gráfica, banco de dados ou bibliotecas externas avançadas;
- Dados mantidos em memória (vetores/structs) durante a execução;
- Nenhum dado clínico individual armazenado;
- Código modularizado em funções, sem concentrar lógica na `main`;
- Mensagens claras de confirmação e erro.

## Funcionalidades implementadas (Etapa 2)

Menu principal, que se repete até o usuário escolher encerrar:

| Opção | Funcionalidade |
|---|---|
| 1 | Cadastrar ação |
| 2 | Listar ações |
| 3 | Pesquisar ação (código, escola ou tema) |
| 4 | Atualizar situação da ação |
| 5 | Gerar resumo geral |
| 6 | Encerrar |

Validações e tratamentos de erro implementados:

- Código da ação aceita **somente números** inteiros maiores que zero;
- Código duplicado, campos obrigatórios vazios, quantidades negativas ou não numéricas, data fora do formato DD/MM/AAAA e opções inexistentes no menu;
- Registro inexistente (ao pesquisar ou atualizar) e limite de armazenamento atingido (50 ações).

## Como compilar e executar

**Dev-C++:** abra o arquivo `src/main.c` e aperte **F11** (Compilar e Executar).

**gcc (terminal):**

```bash
Pelo terminal, utilizando GCC:

gcc -o pse_em_acao src/main.c

No Windows:

.\pse_em_acao.exe

No Linux ou macOS:

./pse_em_acao

Após iniciar o programa, o usuário poderá acessar as funcionalidades pelo menu.
```

O código é escrito em C simples (padrão C89), sem bibliotecas externas, e os textos do programa não usam acentos para evitar problemas de exibição no terminal do Windows.

## Limitações conhecidas

- Os dados ficam apenas em memória: ao encerrar o programa, as ações cadastradas são perdidas;
- Capacidade máxima de 100 ações por execução;
- A busca por escola e tema diferencia maiúsculas de minúsculas;
- Depois de cadastrada, a ação só pode ter a situação alterada (não há edição de outros campos nem exclusão).

## Vídeo de apresentação

[inserir link do vídeo]
