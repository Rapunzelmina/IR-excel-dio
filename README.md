[Uploading README.md…]()
# 📊 Agregador de Dados para Imposto de Renda (Excel)

Ferramenta em Excel para organizar os rendimentos do ano e reunir, em um só lugar, as informações necessárias para a declaração de Imposto de Renda. Projeto do desafio da **DIO**.

## 🎯 Objetivo

Substituir anotações soltas por uma planilha com **menu de navegação**, **validação automática de entradas**, **resumo com gráfico** e **links rápidos** para os portais oficiais.

## 🗂️ Estrutura da planilha

| Aba | Função |
|---|---|
| **Menu** | Tela inicial com botões (hiperlinks internos) para cada aba |
| **Rendimentos** | Cadastro dos lançamentos (até 500 linhas) com validações |
| **Resumo** | Totais por categoria e por mês, conferência e gráfico |
| **Links** | Atalhos: Receita Federal, e-CAC, gov.br, programa IRPF |
| **Listas** | Dados de apoio que alimentam as listas suspensas |

## ✅ Validações de dados

| Campo | Regra |
|---|---|
| Data | Somente datas dentro do ano-base (01/01/2025 a 31/12/2025) |
| CPF/CNPJ | Texto com 11 a 14 dígitos |
| Categoria | Lista suspensa (aba Listas) |
| Valor bruto / IR retido | Número maior ou igual a zero |

Entradas inválidas exibem mensagem de erro e são bloqueadas.

## 🧮 Fórmulas utilizadas

- `INDEX` + `MONTH`: converte a data no nome do mês
- `SUMIFS`: soma por categoria e por mês
- `COUNTIFS`: conta lançamentos por categoria
- `SUM`, `IF`, `ROUND`: totais e conferência (aba Resumo, célula B14)

## 🚀 Como usar

1. Baixe `IR_Agregador_de_Dados.xlsx` e abra no Excel.
2. No **Menu**, clique em *Lançar rendimentos*.
3. Preencha as células em **azul** (a linha 5 é um exemplo; sobrescreva).
4. Veja os totais em *Ver resumo*.
5. Use *Links rápidos* para acessar os portais oficiais.

## 📸 Capturas de tela

Adicione seus prints na pasta `/images`:

![Menu](images/menu.png)
![Rendimentos](images/rendimentos.png)
![Resumo](images/resumo.png)

## 🧠 O que aprendi

- Criar menus de navegação com hiperlinks internos
- Aplicar validação de dados (data, lista, texto, número)
- Usar `SUMIFS` e `COUNTIFS` para consolidar informações
- Montar gráfico dinâmico a partir de fórmulas
- Documentar o processo no GitHub com Markdown

## ⚠️ Aviso

Ferramenta de apoio à organização. Não substitui o programa oficial da Receita Federal nem orientação contábil.

## 🔮 Próximos passos

Abas de Deduções, Bens e Direitos e Dívidas.
