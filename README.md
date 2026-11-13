# PSE em Ação — Sistema de Apoio à Vacinação Escolar

Sistema em linguagem C, executado em terminal, para apoiar o planejamento, registro e acompanhamento de ações de vacinação escolar realizadas no âmbito do **Programa Saúde na Escola (PSE)**.

Atividade Extensionista Prática (AEP) — 2º Semestre de 2026
Curso: 

## Integrantes

Arthur da Silva Mota – RA 26002999-2 

João Fábio Pires Parra – RA 26006728-2 

Lucas Masaki Sversuti – RA 26002032-2 


## Descrição do projeto

O Programa Saúde na Escola (PSE) inclui, entre suas ações prioritárias, a verificação da situação vacinal de estudantes da rede pública. Apesar dos avanços recentes na integração entre saúde e educação, a execução dessas ações ainda enfrenta desafios de comunicação, planejamento e acompanhamento, muitas vezes registradas em anotações e planilhas dispersas.

Este projeto propõe uma aplicação simples em C, executada em terminal, capaz de:

- Cadastrar ações de vacinação (código, escola, tema, data prevista, público-alvo, responsável, quantidade prevista);
- Listar e pesquisar ações por código, escola ou tema;
- Atualizar a situação de uma ação (planejada, realizada ou cancelada) e registrar a quantidade efetiva de participantes;
- Gerar um resumo geral com quantidade de ações por situação e percentual de participação.

O sistema **não coleta nem armazena dados clínicos individuais** de estudantes (nome, diagnóstico, prontuário), trabalhando apenas com informações coletivas e fictícias sobre as ações planejadas, sem substituir o trabalho de profissionais de saúde.

### Requisitos funcionais (resumo)

| Código | Descrição |
|---|---|
| RF01 | Cadastro de ação de vacinação |
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
| 1 | Cadastrar ação de vacinação |
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
gcc -o pse_em_acao src/main.c
./pse_em_acao        # no Windows: pse_em_acao.exe
```

O código é escrito em C simples (padrão C89), sem bibliotecas externas, e os textos do programa não usam acentos para evitar problemas de exibição no terminal do Windows.

## Organização das pastas

```
.
├── README.md
├── docs/
│   ├── AEP_Etapa1_PSE_Vacinacao.pdf              # Documento escrito da Etapa 1 (formatação ABNT)
│   ├── AEP_Etapa2_PSE_Vacinacao.pdf              # Documento final escrito da Etapa 2 (formatação ABNT)
│   ├── requisitos/                                # Requisitos funcionais e não funcionais
│   ├── diagramas/                                 # Fluxogramas (menu principal e cadastro de ação) e diagrama de casos de uso
│   └── pseudocodigo/                              # Pseudocódigos do menu principal e do cadastro
├── src/                                            # Código-fonte em C (Etapa 2)
│   └── main.c
└── manual/                                         # Manual do usuário e capturas de tela (Etapa 2)
```


## Vídeo de apresentação

[inserir link do vídeo]
