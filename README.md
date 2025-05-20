# Documentação da Linguagem LSP - Linguagem Sênior de Programação

Sênior Sistemas

- Documentação da Linguagem LSP - <https://documentacao.senior.com.br/tecnologia>

## Índice

- [Introdução](#Introdução)
- [Sintaxe e Estrutura](#sintaxe-e-estrutura)
  * [Estrutura Básica](#estrutura-básica)
  * [Case Sensitivity](#case-sensitivity)
  * [Identação e Espaçamento](#identação-e-espaçamento)
  * [Estruturas de Bloco](#estruturas-de-bloco)
- [Caracteres com Comportamento Especial](#caracteres-com-comportamento-especial)
- [Comentários](#comentários)
- [Palavras Reservadas](#palavras-reservadas)
- [Variáveis de Sistema](#variáveis-de-sistema)
- [Operadores](#operadores)
  * [Operadores Lógicos](#operadores-lógicos)
  * [Operadores Aritméticos](#operadores-aritméticos)
  * [Operadores Extras](#operadores-extras)
  * [Observação sobre o operador %](#observação-sobre-o-operador-%)
  * [Comportamentos Especiais](#comportamentos-especiais)
- [Tipo de Dados e Variáveis](#tipo-de-dados-e-variáveis)
  * [Tipos de Dados](#tipos-de-dados)
  * [Declaração ou Definição de Variáveis](#declaração-ou-definição-de-variáveis)
  * [Declaração ou Definição de Variáveis com Tamanho](#declaração-ou-definição-de-variáveis-com-tamanho)
  * [Forma de Acesso](#forma-de-acesso)
  * [Regras](#regras)
- [Manipulação de Alfa](#manipulação-de-alfa)
  * [CopiarAlfa e CopiarStr](#copiaralfa-e-copiarstr)
  * [TamanhoAlfa e TamanhoStr](#tamanhoalfa-e-tamanhostr)
  * [PosicaoAlfa e PosicaoStr](#posicaoalfa-e-posicaostr)
  * [SubstAlfa e SubstAlfaUmaVez](#substalfa-e-substalfaumavez)
  * [Concatenar](#concatenar)
- [Cast de Variável](#cast-de-variável)
  * [AlfaParaData](#alfaparadata)
  * [AlfaParaDecimal](#alfaparadecimal)
  * [AlfaParaInt](#alfaparaint)
  * [IntParaAlfa](#intparaalfa)
  * [ConverteMascara](#convertemascara)
  * [Concatenação de Strings](#concatenação-de-strings)
  * [Quebra de Linha](#quebra-de-linha)
- [Manipulação de Datas](#manipulação-de-datas)
  * [DataHoje](#datahoje)
  * [AdicionarDias](#adicionardias)
  * [FormatarData](#formatardata)
- [Arredondamento de Valores](#arredondamento-de-valores)
  * [Arredondar](#arredondar)
  * [Truncar](#truncar)
- [Mensagens](#mensagens)
- [Cancel](#cancel)
- [Padrões e Boas Práticas](#padrões-e-boas-práticas)
  * [Boas Práticas e Regras Gerais](#boas-práticas-e-regras-gerais)
  * [Declaração de Variáveis](#declaração-de-variáveis)
  * [Padrão de Nomenclatura de Variáveis](#padrão-de-nomenclatura-de-variáveis)
  * [Identação e Espaçamento](#identação-e-espaçamento)
  * [Estruturas de Bloco](#estruturas-de-bloco)
  * [Comentários](#comentários)
- [Controle de Fluxo](#controle-de-fluxo)
  * [Condicionais](#condicionais)
  * [Estrutura de Repetição](#estrutura-de-repetição)
  * [Pare](#pare)
  * [VaPara](#vapara)
  * [Recursividade](#recursividade)
- [Definição de Arrays](#definição-de-arrays)
  * [Declaração de Arrays](#declaração-de-arrays)
  * [Atribuição de Valores](#atribuição-de-valores)
  * [Acesso aos Valores](#acesso-aos-valores)
  * [Iteração sobre Arrays](#iteração-sobre-arrays)
  * [Exemplo Completo](#exemplo-completo)
- [Definição de Listas](#definição-de-listas)
  * [Comandos para Definição de Listas](#comandos-para-definição-de-listas)
  * [Acesso aos Campos](#acesso-aos-campos)
  * [Comandos para Manipulação de Registros](#comandos-para-manipulação-de-registros)
  * [Comandos para Posicionamento de Listas](#comandos-para-posicionamento-de-listas)
  * [Comandos para Procura de Registros](#comandos-para-procura-de-registros)
  * [Comandos para Posicionamento Absoluto](#comandos-para-posicionamento-absoluto)
  * [Comandos Diversos de Listas](#comandos-diversos-de-listas)
  * [Exemplo](#exemplo)
  * [Atribuição de Valores para a Lista](#atribuição-de-valores-para-a-lista)
  * [Utilização de Dados de uma Lista](#utilização-de-dados-de-uma-lista)
  * [Exclusão de Dados da Lista](#exclusão-de-dados-da-lista)
  * [Algoritmos de Leitura de Dados da Lista](#algoritmos-de-leitura-de-dados-da-lista)
    + [Utilizando o Retorno das Funções](#utilizando-o-retorno-das-funções)
    + [Utilizando Propriedade Indicadora de Fim de Arquivo (FDA)](#utilizando-propriedade-indicadora-de-fim-de-arquivo-fda)
    + [Utilizando Diretamente o Retorno das Funções de Movimentação](#utilizando-diretamente-o-retorno-das-funções-de-movimentação)
- [Definição de Tabelas](#definição-de-tabelas)
  * [Sintaxe](#sintaxe)
  * [Exemplo](#exemplo)
  * [Forma de Acesso à Variável](#forma-de-acesso-à-variável)
- [Definição de Cursor](#definição-de-cursor)
  * [Cursor Simples](#cursor-simples)
  * [Cursor Completo](#cursor-completo)
  * [Vantagens e Desvantagens dos Cursores](#vantagens-e-desvantagens-dos-cursores)
    + [Cursor Simples](#cursor-simples)
    + [Cursor Completo](#cursor-completo)
- [Definição de Funções](#definição-de-funções)
  * [Exemplos de Funções](#exemplos-de-funções)
    + [Função Simples](#função-simples)
    + [Função com Parâmetro Numérico](#função-com-parâmetro-numérico)
    + [Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro](#função-com-parâmetro-numérico-e-retorno-no-mesmo-parâmetro)
    + [Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica](#função-com-dois-parâmetros-numéricos-e-retorno-em-uma-variável-específica)
  * [Organização das Funções](#organização-das-funões)
- [Retorno para Aplicação](#retorno-para-aplicação)
  * [ValRet](#valret)
  * [ValStr](#valstr)
- [Funções Gerais](#funções-gerais)
- [Funções SQL](#funções-sql)
  * [SQL Senior 2](#sql-senior-2)
    + [Ativação da Linguagem](#ativação-da-linguagem)
    + [Restrições](#restrições)
  * [Exemplos](#exemplos)
    + [Utilização de INSERT](#utilização-de-insert)
    + [Utilização de SELECT](#utilização-de-select)
    + [Utilização de UPDATE](#utilização-de-update)
  * [Passagem de Parâmetros](#passagem-de-parâmetros)
    + [Exemplo com `__inserir`](#exemplo-com-inserir)
    + [Exemplo com `SQL_Definir<tipo_variavel>`](#exemplo-com-sql-definir-tipo-variavel)
- [Manipulação de Arquivos](#manipulação-de-arquivos)
  * [Abrir (Open)](#abrir-open)
  * [Ler (Read)](#ler-read)
  * [Lernl (ReadLn)](#lernl-readln)
  * [Gravar (Write)](#gravar-write)
  * [Gravarnl (WriteLn)](#gravarnl-writeln)
  * [Fechar (Close)](#fechar-close)
- [Chamada de Web Service](#chamada-de-web-service)
  * [Modos de Execução](#modos-de-execução)
  * [WS-Security](#ws-security)
  * [Autenticação](#autenticação)
- [Chamada HTTP](#chamada-http)
  * [Funções para Requisições HTTP](#funções-para-requisições-http)
  * [Exemplos de Código](#exemplos-de-c-digo)
    + [Exemplo 1: Busca o CEP na API VIA CEP](#exemplo-1-busca-o-cep-na-api-via-cep)
    + [Exemplo 2: Busca a Cidade na API IBGE](#exemplo-2-busca-a-cidade-na-api-ibge)

## Introdução

A Linguagem Senior de Programação (LSP) é uma linguagem proprietária utilizada nos sistemas da Senior para a customização e extensão de funcionalidades. Ela permite a manipulação de dados, a criação de regras de negócio personalizadas e a automação de processos dentro do ambiente Senior.

Diferente de linguagens tradicionais como Java, C# ou Python, a LSP foi projetada especificamente para interagir com os sistemas Senior, possuindo sintaxe e estrutura próprias. Seu uso é essencial para desenvolvedores que desejam criar soluções personalizadas dentro da plataforma.

Nesta documentação, abordaremos a sintaxe, estrutura, operadores, controle de fluxo, manipulação de arquivos, chamadas de web service e outros aspectos da linguagem, sempre com exemplos práticos para facilitar a compreensão.

## Sintaxe e Estrutura

A linguagem LSP possui uma sintaxe própria, estruturada para facilitar a criação de regras de negócio dentro do ecossistema da Senior. Os comandos são escritos de forma sequencial e utilizam palavras-chave específicas para definir ações e estruturas de controle.

### Estrutura Básica

Cada comando na LSP deve ser finalizado com um ponto e vírgula (`;`). O código deve seguir uma ordem lógica para garantir a execução correta.

Exemplo de um código básico na LSP:

```lsp
Definir Numero vnX;
Definir Numero vnY;
Definir Numero vnResultado;
vnX = 10;
vnY = 20;
vnResultado = vnX + vnY;
Mensagem(Retorna, vnResultado);
```

### Case Sensitivity

A LSP **não** diferencia maiúsculas de minúsculas na declaração de variáveis. Isso significa que os seguintes exemplos são equivalentes:

```lsp
Definir Alfa vaNomeVariavel;
Definir Alfa VANOMEVARIAVEL;
```

### Identação e Espaçamento

A identação padrão na LSP é de **2 espaços** ao invés de 4. 

```lsp
Definir Numero vnX;
Definir Numero vnY;
Definir Numero vnSoma;
vnX = 5;
vnY = 15;

Se (vnX < vnY) { 
  vnSoma = vnX + vnY;
}
```

### Estruturas de Bloco

Regras:

   - Se o bloco contiver apenas uma linha, não é necessário informar `{ }` ou `inicio;` e `fim;`, basta adicionar identado na linha de baixo e identado.
   - Os blocos de código em LSP devem ser delimitados com `{ }`, ou alternativamente com `inicio;` e `fim;` (menos comum). 
   - Todas as condições ou estruturas de repetições devem estar entre parênteses `()`.

Exemplo de estrutura de bloco com apenas uma linha:

```lsp
Se (_condição_) 
  vn = 1; @ Estrutura do bloco em uma linha @
```

Exemplo de estrutura de bloco com `{ }`:

```lsp
Se (_condição_) {
  @ Estrutura do bloco @
}
```

Exemplo de estrutura de bloco com `inicio;` e `fim;`:

```lsp
Se (_condição_) 
Inicio
  @ Estrutura do bloco @
Fim;
```

Exemplo de estrutura de bloco Incorreto:

```lsp
Se vnX < vnY {
  @ Estrutura do bloco @
}

@ OU @

Se vnX < vnY 
Inicio
  @ Estrutura do bloco @
Fim;
```

## Caracteres com Comportamento Especial

Existem determinados caracteres que, quando inseridos em uma expressão literal nas regras, devem ser precedidos do caractere `\` (barra) para indicar que estes caracteres serão usados literalmente e não como caracteres especiais. Estes caracteres são: `"` (aspas) e `\` (barra).

Exemplo:

```lsp
EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");
```

## Comentários

Comentários são utilizados para explicar o código e são ignorados pelo compilador. Existem três tipos de comentários na LSP:

- Comentário de uma linha: Utiliza o símbolo `@`.
- Comentário de múltiplas linhas: Inicia com `/*` e termina com `*/`.

Exemplo de comentário de uma linha:

```lsp
@ Este é um comentário de uma linha
Definir Numero vnX;
```

Exemplo de comentário de múltiplas linhas:

```lsp
/*
  Este é um comentário
  de múltiplas linhas
*/
Definir Numero vnX;
```

## Palavras Reservadas

A LSP não faz distinção de letras maiúsculas e minúsculas. Portanto, a LSP possui 51 (cinquenta e uma) palavras reservadas que não poderão ser usadas pelo programador para outros fins.

- Definir
- Se
- Senao
- Enquanto
- Para
- Funcao
- Fim
- Inicio
- Mensagem
- Cancel
- ValRet
- ValStr
- VaPara

| Comando | Descrição |
| --- | --- |
| Se (If) | Comando de comparação/pergunta, com resposta verdadeiro ou falso. |
| Senao (Else) | É a saída da pergunta (Se) quando a resposta for falsa. |
| e (And) | Liga duas ou mais condições, devendo todas serem verdadeiras para o resultado ser verdadeiro. |
| ou (Or) | Liga duas ou mais condições, bastando uma ser verdadeira para o resultado ser verdadeiro. |
| Inicio (Begin ou "{" - abre chaves) | Marcador utilizado para iniciar um bloco. |
| Fim; (End ou "}" - fecha chaves) | Marcador utilizado para finalizar um bloco. |
| Para (For) | Comando utilzado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes. Indica-se um \<valor inicial\> e esse valor é incrementado pelo valor do \<contador\> até que a \<condicao\> seja falsa. Sintaxe: Para (\<valor inicial\>; \<condicao\>; \<contador\>); |
| Enquanto (While) | Comando utilizado para se fazer um loop de comandos. Ou seja, fazer com que um bloco de comandos seja executado determinado número de vezes até que a \<condição>, seja falsa. Sintaxe: Enquanto (\<condicao\>); |
| Pare (Break) | Interrompe a execução de um bloco do comando Para ou Enquanto. O Pare, simplesmente faz com que o sistema abandone o bloco de comandos e continue a execução do restante das regras. Sintaxe: Pare;|
| Cancel (1) | Se for utilizado em uma regra do evento "Antes de Imprimir" de uma seção, cancela a impressão da seção. Se for usado no evento "Na Impressão" de um campo, cancela a impressão deste campo. Sintaxe: Cancel (1); |
| Cancel (2) | Deve ser usado em conjunto com as variáveis de sistema ValStr ou ValRet e somente no Evento "Na Impressão". O valor alfa atribuído para ValStr seguido de Cancel (2) será impresso no campo em que foi implementada a regra. Sintaxe: Cancel (2); |
| Cancel (3) | Utilizado apenas em controles do tipo fórmula (na ordenação por fórmula) para excluir o registro atual do relatório (semelhante a executar o Cancel(1) nas regras: Definição\Seleção, Detalhe\Antes_de_Imprimir e Detalhe\Depois_de_Imprimir) |
| Mensagem (Printf) | Exibe uma mensagem para o usuário durante a execução da regra. Sintaxe: Mensagem (\<tipo_da_mensagem\>,"\<mensagem\>"); |
| Vapara (Goto) | Desvia a execução da regra para o \<rótulo\> determinado. Sintaxe: Vapara \<rótulo\>; |
| Regra (Rule) | Chama uma outra regra, identificada pelo \<número da regra\>. Sintaxe: Regra (\<numero_da_regra\>); |
| Continue | Continua a execução de um loop feito pelo comando Para. Ou seja, se quiser que o loop não seja executado em determinado caso, faça o teste da condição e com ela use o comando. Sintaxe: Continue; |
| End (Var) | Usado na definição de uma função, para indicar qual parâmetro retornará valor. Sintaxe: Funcao Teste (end \<tipo do parâmetro\> \<nome do parâmetro\>); |
| Abrir (Open) |	Abre o \<arquivo informado\>, no \<modo de abertura\> desejado. Se o arquivo não existir ele é criado. Ele retorna um manipulador de arquivos. Sintaxe: Manipulador_de_Arquivo = Abrir (“\<nome_do_arquivo\>”,\<modo_de_abertura\>); Onde o Modo de Abertura pode ser: Ler ou Gravar. |
| Fechar (Close) |	Fecha o arquivo aberto pela função Abrir. Sintaxe: Fechar (\<manipulador_de_arquivo\>); |
| Ler (Read) |	Lê uma \<quantidade de caracteres\> do arquivo especificado no \<manipulador de arquivo\> e joga o valor lido em uma \<variável\>. Sintaxe: Ler (\<manipulador_de_arquivos\>, \<variavel\>,\<tamanho\>); |
| Gravar (Write) |	Grava o valor de uma \<variável ou de uma constante> no \<manipulador de arquivos\>. Sintaxe: Gravar (\<manipulador_de_arquivos\>,\<variável ou constante>,\<tamanho\>); |
| Lernl (ReadLn) |	Lê uma linha no arquivo indicado pelo \<manipulador de arquivos\> e joga o valor lido em uma \<variável\>. Sintaxe: Lernl (\<manipulador_de_arquivos\>,\<variável\>); |
| Gravarnl (WriteLn) |	Grava uma linha no arquivo indicado pelo \<manipulador de arquivos\> com o valor contido na variável especificada. Sintaxe: Gravarnl (\<manipulador_de_arquivos\>,\<variável ou constante\>); |
| Inserir (Include) |	Faz com que o sistema, insira um arquivo na regra atual, em tempo de execução/compilação. Sintaxe: Inserir “\<nome_arquivo\>”; ou Inserir "Header.lsp"; |
| ValStr |	Usado apenas no gerador, para alterar a descrição de um campo tipo Descrição. O texto passada para ValStr será impresso no lugar da descrição original do campo. ValStr = "Teste"; Cancel(2);	|
| Cursor |	Os cursores nada mais são que um SELECT em uma regra, retornando registros que satisfaçam a condição informada na propriedade SQL de um Cursor. Observações: O SELECT utilizado no cursor não possui relacionamento direto com o SELECT utilizado pelo gerador de relatórios, por exemplo. |

## Variáveis de Sistema

As variáveis de sistema são utilizadas para obter informações do ambiente de execução, como data, hora, usuário, entre outros. Abaixo estão algumas das principais variáveis de sistema disponíveis no Gerador de Relatórios:

| Variável       | Descrição                                                |
|----------------|----------------------------------------------------------|
| AnoSis         | Ano do sistema operacional                               |
| CodEmp         | Código da empresa                                        |
| CodFil         | Código da Filial                                         |
| CodUsu         | Código do usuário                                        |
| DatSis         | Data do sistema operacional                              |
| DBNomeUsuario  | Nome do usuário do banco de dados                        |
| DBTipo         | Banco de dados utilizado (ORACLE/SQLSERVER/POSTGRESQL/OUTRO) |
| DesRodape      | Descrição para rodapé                                    |
| DiaSis         | Dia do sistema operacional                               |
| Empresa        | Nome da empresa                                          |
| ExtSis         | Data por extenso do sistema operacional                  |
| Filial         | Nome da filial                                           |
| GerTabAlf      | Variável alfanumérica com 2000 ocorrências               |
| GerTabNum      | Variável numérica flutuante com 999 ocorrências          |
| HorSis         | Hora do sistema operacional                              |
| MesSis         | Mês do sistema operacional                               |
| NomUsu         | Nome do usuário                                          |
| NumPag         | Número da página                                         |
| QtdDupPag      | Quantidade de duplicatas impressas por página - Utilizado no modelo FRCR002 |

## Operadores

### Operadores Lógicos

Os operadores lógicos são utilizados para realizar comparações e operações lógicas. Os principais operadores lógicos são:

- `=`: Igual
- `<>`: Diferente
- `>`: Maior que
- `<`: Menor que
- `>=`: Maior ou igual a
- `<=`: Menor ou igual a
- `e`: E lógico
- `ou`: Ou lógico

### Operadores Aritméticos

Os operadores aritméticos são utilizados para realizar operações matemáticas. Os principais operadores aritméticos são:

- `+`: Adição
- `-`: Subtração
- `*`: Multiplicação
- `/`: Divisão
- `++`: Incremento de 1
- `--`: Decremento de 1

### Operadores Extras

Os operadores extras são utilizados para outras operações específicas. Alguns dos operadores extras são:

- `/*`: Início de comentário de múltiplas linhas
- `*/`: Fim de comentário de múltiplas linhas
- `@`: Comentário de uma linha

#### Observação sobre o operador %

O operador % (módulo) não existe na LSP. Para obter o resto da divisão, deve-se utilizar a função `RestoDivisao`.

Exemplo de uso da função RestoDivisao:
```lsp
Definir Numero vnDividendo;
Definir Numero vnDivisor;
Definir Numero vnResto;

vnDividendo = 1500;
vnDivisor = 400;

RestoDivisao(vnDividendo, vnDivisor, vnResto);
@ vnResto será 300 @
```

A função RestoDivisao retorna o resto da divisão de um número por outro. Os valores de entrada devem ser obrigatoriamente inteiros iguais ou maiores que 1. Por exemplo: ao informar 0.2, será considerado somente 0. Ao informar 1.1 será considerado 1.

Sintaxe: RestoDivisao(Dividendo, Divisor, Resto);

Parâmetros:
- Dividendo: Campo/Variável que será dividido
- Divisor: Campo/Variável pelo qual o Dividendo será dividido
- Resto: Variável que receberá o resto da divisão 

### Comportamentos Especiais

Existem determinados caracteres que, quando inseridos em uma expressão literal nas regras, devem ser precedidos do caractere `\` (barra) para indicar que estes caracteres serão usados literalmente e não como caracteres especiais. Estes caracteres são: `"` (aspas) e `\` (barra).

Exemplo:

```lsp
EnviaEMail("Joao","joao@senior.com.br", "", "", "Teste","\"\\\\Servidor\\teste.txt\"", "");
```

## Tipo de Dados e Variáveis

### Tipos de Dados

Os tipos de dados suportados pela LSP são:

- **Alfa**: Cadeia de caracteres.
- **Numero**: Números inteiros ou decimais.
- **Data**: Datas.
- **Lista**: Lista dinâmica nas regras.
- **Tabela**: Estrutura semelhante a um objeto em JavaScript.
- **Grid**: Estrutura de grade.
- **Cursor**: Estrutura para manipulação de consultas SQL.
- **Funcao**: Funções definidas pelo usuário.

### Declaração ou Definição de Variáveis

As variáveis na LSP são declaradas utilizando o comando `Definir`. O nome das variáveis deve ter no máximo 100 caracteres e pode conter `_` (sublinhado). Não é permitido usar acentuação no nome das variáveis. Caso a variável não seja definida, esta será considerada como tipo Numero.

Exemplo de declaração de variáveis:

Sintaxe

Definir <Tipo> <Nome_da_Variável>;

```lsp
Definir Alfa vaNome;
Definir Numero vnIdade;
Definir Data vdNascimento;
```

### Declaração ou Definição de Variáveis com Tamanho

Para variáveis do tipo `Alfa`, é possível definir o tamanho máximo da cadeia de caracteres.

Exemplo:

```lsp
Definir Alfa vaNome[30];
```

### Forma de Acesso

As variáveis são acessadas diretamente pelo seu nome.

Exemplo:

```lsp
vaNome = "João";
vnIdade = 25;
```

As variáveis com tamanhos(Arrays) são acessadas diretamente pelo seu índice.

   - O Índice pode conter um valor fixo, uma variável ou uma formula

<Nome_da_Variável>[<índice>] = <valor_atribuído>;

Exemplo:

```lsp
Definir Alfa vaNome[30];
Definir Numero vnIndice;

vnIndice = 1;

@ Valor Fixo @
vaNome[1] = "Nome";

@ Valor Variável @
vaNome[vnIndice] = "Nome";

@ Valor Formula @
vaNome[vnIndice + 1 * 2 ] = "Nome";
```

### Regras

- Variaveis do tipo Data deve-se usar a função MontaData(dd,mm,yyyy,vdData); para atribuir uma data ou atribuir a variável de sistema DatSis
- O nome das variáveis não pode ser igual ao nome dos parâmetros de funções. 
- O nome das variáveis não pode ser igual ao nome dos campos de listas.


## Manipulação de Alfa

As funções de manipulação de strings na LSP permitem realizar operações comuns como copiar, medir, encontrar e substituir partes de strings.

### CopiarAlfa e CopiarStr

Estas funções copiam parte do conteúdo de uma variável/campo alfanumérico para outra variável alfanumérica.

**Sintaxe:**

```lsp
CopiarAlfa(<origem>, <destino>, <posicao>, <tamanho>);
CopiarStr(<origem>, <destino>, <posicao>, <tamanho>);
```

**Exemplo:**

```lsp
Definir Alfa vaOrigem;
Definir Alfa vaDestino;

vaOrigem = "Exemplo de string";
CopiarAlfa(vaOrigem, vaDestino, 1, 7); @ vaDestino será "Exemplo" @
```

### TamanhoAlfa e TamanhoStr

Estas funções retornam o tamanho de uma variável/campo alfanumérico.

**Sintaxe:**

```lsp
TamanhoAlfa(<origem>);
TamanhoStr(<origem>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnTamanho;

vaTexto = "Exemplo";
vnTamanho = TamanhoAlfa(vaTexto); @ vnTamanho será 7 @
```

### PosicaoAlfa e PosicaoStr

Estas funções procuram por uma parte de texto dentro de um campo/variável do tipo Alfa, retornando a posição em que o texto inicia.

**Sintaxe:**

```lsp
PosicaoAlfa(<texto>, <subtexto>);
PosicaoStr(<texto>, <subtexto>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnPosicao;

vaTexto = "Exemplo de string";
vnPosicao = PosicaoAlfa(vaTexto, "de"); @ vnPosicao será 9 @
```

### SubstAlfa e SubstAlfaUmaVez

Estas funções substituem um trecho específico dentro de um texto por outro texto.

**Sintaxe:**

```lsp
SubstAlfa(<texto>, <subtexto>, <novoTexto>);
SubstAlfaUmaVez(<texto>, <subtexto>, <novoTexto>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;

vaTexto = "Exemplo de string";
SubstAlfa(vaTexto, "string", "texto"); @ vaTexto será "Exemplo de texto" @
```

### Concatenar

Esta função concatena duas ou mais strings.

**Sintaxe:**

```lsp
Concatenar(<texto1>, <texto2>, ...);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto1;
Definir Alfa vaTexto2;
Definir Alfa vaResultado;

vaTexto1 = "Exemplo";
vaTexto2 = " de string";
vaResultado = Concatenar(vaTexto1, vaTexto2); @ vaResultado será "Exemplo de string" @
```

## Cast de Variável

As funções de cast de variável na LSP permitem converter valores entre diferentes tipos de dados.

### AlfaParaData

Converte um valor alfanumérico para o tipo Data.

**Sintaxe:**

```lsp
AlfaParaData(<texto>, <data>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Data vdData;

vaTexto = "01/01/2020";
AlfaParaData(vaTexto, vdData); @ vdData será 01/01/2020 @
```

### AlfaParaDecimal

Converte um valor alfanumérico para o tipo Decimal.

**Sintaxe:**

```lsp
AlfaParaDecimal(<texto>, <decimal>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Decimal vdDecimal;

vaTexto = "123.45";
AlfaParaDecimal(vaTexto, vdDecimal); @ vdDecimal será 123.45 @
```

### AlfaParaInt

Converte um valor alfanumérico para o tipo Inteiro.

**Sintaxe:**

```lsp
AlfaParaInt(<texto>, <inteiro>);
```

**Exemplo:**

```lsp
Definir Alfa vaTexto;
Definir Numero vnInteiro;

vaTexto = "123";
AlfaParaInt(vaTexto, vnInteiro); @ vnInteiro será 123 @
```

### IntParaAlfa

Converte um valor inteiro para o tipo Alfanumérico.

**Sintaxe:**

```lsp
IntParaAlfa(<inteiro>, <texto>);
```

**Exemplo:**

```lsp
Definir Numero vnInteiro;
Definir Alfa vaTexto;

vnInteiro = 123;
IntParaAlfa(vnInteiro, vaTexto); @ vaTexto será "123" @
```

### ConverteMascara

Converte um valor de entrada (numérico, data, hora ou cadeia de caracteres) para o tipo de dado cadeia de caracteres.

**Sintaxe:**

```lsp
ConverteMascara(<tipo>, <valor>, <texto>, <mascara>);
```

**Exemplo:**

```lsp
Definir Numero vnNumero;
Definir Alfa vaTexto;

vnNumero = 123456;
ConverteMascara(1, vnNumero, vaTexto, "999.999"); @ vaTexto será "123.456" @
```

#### Concatenação de Strings

Na LSP, não é possível concatenar diretamente uma variável do tipo Numero com uma variável do tipo Alfa. Para realizar essa operação, é necessário:

1. Definir uma variável Alfa com o mesmo nome da variável numérica, mudando apenas o prefixo de `vn` para `va`
2. Utilizar a função `IntParaAlfa()` para converter o valor numérico em string

Exemplo:
```lsp
Definir Numero vnNumero;
Definir Alfa vaNumero;
Definir Alfa vaResultado;

vnNumero = 10;
IntParaAlfa(vnNumero, vaNumero);
vaResultado = "O número é " + vaNumero;
```

#### Quebra de Linha

Na LSP, não existe o caractere `\n` para quebra de linha. Para realizar a quebra de linha em uma string, deve-se:

1. Definir uma variável Alfa para armazenar o caractere de quebra de linha
2. Utilizar a função `CaracterParaAlfa(13, vaEnter)` para obter o caractere de quebra de linha (13 na tabela ASCII)
3. Concatenar essa variável na string onde se deseja a quebra de linha

Exemplo:
```lsp
Definir Alfa vaEnter;
Definir Alfa vaMensagem;

CaracterParaAlfa(13, vaEnter);
vaMensagem = "Primeira linha" + vaEnter + "Segunda linha";
``` 

## Manipulação de Datas

As funções de manipulação de datas na LSP permitem realizar operações comuns como obter a data atual, adicionar dias e formatar datas.

### DataHoje

Retorna a data atual do sistema operacional.

**Sintaxe:**

```lsp
DataHoje(<data>);
```

**Exemplo:**

```lsp
Definir Data vdData;

DataHoje(vdData); @ vdData será a data atual @
```

### AdicionarDias

Adiciona um número de dias a uma data.

**Sintaxe:**

```lsp
AdicionarDias(<data>, <dias>, <novaData>);
```

**Exemplo:**

```lsp
Definir Data vdData;
Definir Data vdNovaData;

vdData = "01/01/2020";
AdicionarDias(vdData, 10, vdNovaData); @ vdNovaData será 11/01/2020 @
```

### FormatarData

Formata uma data para um formato específico.

**Sintaxe:**

```lsp
FormatarData(<data>, <formato>, <texto>);
```

**Exemplo:**

```lsp
Definir Data vdData;
Definir Alfa vaTexto;

vdData = "01/01/2020";
FormatarData(vdData, "dd/MM/yyyy", vaTexto); @ vaTexto será "01/01/2020" @
```

## Arredondamento de Valores

As funções de arredondamento de valores na LSP permitem arredondar números para um número específico de casas decimais.

### Arredondar

Arredonda um número para um número específico de casas decimais.

**Sintaxe:**

```lsp
Arredondar(<numero>, <casasDecimais>, <resultado>);
```

**Exemplo:**

```lsp
Definir Numero vnNumero;
Definir Numero vnResultado;

vnNumero = 123.456;
Arredondar(vnNumero, 2, vnResultado); @ vnResultado será 123.46 @
```

### Truncar

Trunca um número para inteiro, removendo a parte fracionária do número.

**Sintaxe:**

```lsp
Truncar(<numero>, <resultado>);
```

**Exemplo:**

```lsp
Definir Numero vnNumero;
Definir Numero vnResultado;

vnNumero = 123.456;
Truncar(vnNumero, vnResultado); @ vnResultado será 123 @
```

## Mensagens

A função `Mensagem` é utilizada para exibir mensagens ao usuário. Existem diferentes tipos de mensagens, como `Retorna`, `Erro`, e `Refaz`.

1. Não é possível fazer concatenação diretamente no parâmetro da função `Mensagem()`
2. É necessário definir uma variável Alfa antes, fazer as concatenações e atribuir nessa variável
3. A variável Alfa deve ser passada como parâmetro para a função `Mensagem()`


**Sintaxe**

- Mensagem(_tipo_da_mensagem_,"_mensagem_");

Exibe uma mensagem para o usuário. As mensagens possuem características de acordo com o seu tipo.

   - Retorna: Mostra uma mensagem de aviso, com os botões especificados entre colchetes. O símbolo & indica tecla de aceleração (atalho);
   - Erro: Gera uma exceção, mostrando uma mensagem de erro e abortando a execução da regra;
   - Refaz: Gera uma exceção, mostrando uma mensagem de erro e abortando a execução da regra.

- Exemplo comum, quando a mensagem é uma string literal sem concatenação:

```lsp
Mensagem(Retorna, "Operação concluída com sucesso!");
Mensagem(Erro, "Ocorreu um erro na operação.");
```

- Exemplo quando já temos uma variável Alfa com a mensagem final:

```lsp
Definir Alfa vaResultado;
vaResultado = "Mensagem já formatada";
Mensagem(Retorna, vaResultado);
```
- Exemplo quando precisamos fazer concatenação:

```lsp
Definir Alfa vaMensagem;
vaMensagem = "Aluno: " + vaNome + vaEnter + "Média: " + vaMedia;
Mensagem(Retorna, vaMensagem);
```

- Exemplo com botões especificados entre colchetes:

   - Entre colchetes podem conter 1 ou mais parâmetros, o retorno será de acordo com a sequencia do parâmetro, iniciando com 0

```lsp
Definir Numero vnRetorno;

vnRetorno = Mensagem(retorna,"Processo Concluído [&Ok!!!]"); @ O valor da variável vnRetorno será: 0 @

vnRetorno = Mensagem(retorna,"Deseja Sair ? [&Sim,&Não]"); @ O valor da variável vnRetorno será: 0 para Sim e 1 para Não @

vnRetorno = Mensagem(retorna,"Escolha uma opção ? [&Voltar,&Avançar, $Cancelar]"); @ O valor da variável vnRetorno será: 0 para Voltar, 1 para Avançar e 2 para Cancelar @

```

- Exemplo de uso incorreto:

```lsp
Mensagem(Retorna, "Aluno: " + vaNome + vaEnter + "Média: " + vaMedia); @ Erro: concatenação no parâmetro @
```

## Cancel

A função `Cancel` é utilizada para cancelar a execução de uma regra. Dependendo do valor passado como parâmetro, diferentes ações podem ser tomadas. Ao usar a função Cancel(n) em regras que são executadas por eventos de tela, a única ação tomada será o cancelamento da execução da regra, independentemente do valor passado como parâmetro.

Para que seja gerado um erro, deve-se usar a função **Mensagem(Erro, "mensagem")** ou então a equipe de desenvolvimento do sistema deve tratar via código de sistema o retorno de **Cancel(n)**.

No **Gerador de Relatórios**, o comando **Cancel** pode ser usado das seguintes formas:

   - **Cancel(1)**

     Em controles: Cancela a execução da regra e a impressão do mesmo.
     Nas regras: Definição\Seleção e Detalhe\Antes_de_Imprimir, exclui o registro atual do relatório (detalhe);
     Na regra: Definição\Pré-Seleção cancela a execução do relatório.

   - **Cancel(2)**
     Utilizado para imprimir o conteúdo da variável ValStr em controles do tipo descrição e depois sair da regra;

   - **Cancel(3)**
     Utilizado apenas em controles do tipo fórmula (na ordenação por fórmula) para excluir o registro atual do relatório (semelhante a executar o Cancel(1) nas regras: Definição\Seleção, Detalhe\Antes_de_Imprimir e Detalhe\Depois_de_Imprimir).

Exemplo:

```lsp
Cancel(1); @ Cancela a execução da regra e a impressão do controle @
Cancel(2); @ Imprime o conteúdo da variável ValStr em controles do tipo descrição e depois sai da regra @
Cancel(3); @ Exclui o registro atual do relatório em controles do tipo fórmula @
```

## Padrões e Boas Práticas

### Boas Práticas e Regras Gerais

- Sempre termine uma instrução de código com `;`.
- Evite duplicação de código, reutilize funções sempre que possível.
- Mantenha o código modularizado e organizado em funções.
- Utilize nomes descritivos para funções.
- Teste o código extensivamente para garantir que ele funcione corretamente em todas as situações esperadas.

### Declaração de Variáveis

- Declare as variáveis no início do código ou da função.
- Inicialize as variáveis sempre que possível no início do código ou da função.
- Em relatórios, declare e inicialize variáveis nos eventos de Inicialização ou Pré-Seleção.

### Padrão de Nomenclatura de Variáveis

- Utilize nomes descritivos para as variáveis.
- Utilize o padrão CamelCase nos nomes das variáveis.
- Utilize o padrão "v + inicial do tipo de dado" antes do nome da variável:
  - `va` para variáveis do tipo `Alfa`
  - `vn` para variáveis do tipo `Numero`
  - `vd` para variáveis do tipo `Data`
- Evite usar nomes de variáveis que possam ser confundidos com palavras reservadas ou nomes de funções.

### Identação e Espaçamento

- Utilize 2 espaços para identação.
- Mantenha o código organizado e legível, evitando linhas de código muito longas.

### Estruturas de Bloco

- Utilize `{` para abrir um bloco e `}` para fechar um bloco, delimitando assim os blocos de código.
- Se o bloco contiver apenas uma linha, não é necessário informar `{ }`, basta adicionar o código identado na linha de baixo.

Exemplo de estrutura de bloco com apenas uma linha:

```lsp
Se (<Condição>) 
  vn = 1; @ Estrutura do bloco em uma linha @
```

Exemplo de estrutura de bloco com `{ }`:

```lsp
Se (<Condição>) {
  @ Estrutura do bloco @
}
```

### Comentários

- Utilize comentários para explicar o código e facilitar a manutenção.
- Utilize `@` para comentários de uma linha e `/* */` para comentários de múltiplas linhas.

Exemplo de comentário de uma linha:

```lsp
@ Este é um comentário de uma linha @
Definir Numero vnX;
```

Exemplo de comentário de múltiplas linhas:

```lsp
/*
  Este é um comentário
  de múltiplas linhas
*/
Definir Numero vnX;
```

## Controle de Fluxo

### Condicionais

As estruturas condicionais são utilizadas para executar blocos de código com base em condições.

Exemplo de uso do `Se` e `Senao`:

```lsp
Definir Numero vnIdade;
vnIdade = 20;

Se (vnIdade >= 18) {
  Mensagem(Retorna, "Maior de idade");
} Senao {
  Mensagem(Retorna, "Menor de idade");
}
```

### Estrutura de Repetição

As estruturas de repetição são utilizadas para executar blocos de código repetidamente.

Exemplo de uso do `Enquanto`:

```lsp
Definir Numero vnContador;
vnContador = 0;

Enquanto (vnContador < 10) {
  Mensagem(Retorna, vnContador);
  vnContador++;
}
```

Exemplo de uso do `Para`:

```lsp
Para (i = 0; i < 10; i++) {
  Mensagem(Retorna, i);
}
```

### Pare

O comando `Pare` é utilizado para interromper a execução de um bloco de repetição.

Exemplo de uso do `Pare`:

```lsp
Para (vnContador = 0; vnContador < 10; vnContador++) {
  Se (vnContador = 5) {
    Pare;
  }
  Mensagem(Retorna, vnContador);
}
```

### VaPara

O comando `VaPara` é utilizado para desviar a execução do programa para um ponto específico da regra.

Exemplo de uso do `VaPara`:

```lsp
Definir Numero vnIdade;
vnIdade = 20;

Se (vnIdade < 18) {
  VaPara menorDeIdade;
}

Mensagem(Retorna, "Maior de idade");
VaPara fim;

menorDeIdade:
Mensagem(Retorna, "Menor de idade");

fim:
```

### Recursividade

A recursividade é uma técnica de programação onde uma função chama a si mesma para resolver um problema. Em LSP, a recursividade pode ser implementada seguindo alguns padrões específicos.

#### Estrutura Básica de uma Função Recursiva

Uma função recursiva em LSP geralmente possui:
1. Um ou mais casos base (condições de parada)
2. Um ou mais casos recursivos (chamadas à própria função)

Exemplo de implementação recursiva da sequência de Fibonacci:

```lsp
@ Função recursiva para calcular o n-ésimo termo da sequência de Fibonacci @
Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado); {
  @ Caso base 1: primeiro termo @
  Se (vnTermo = 0) {
    vnResultado = vnAnterior;
  } 
  @ Caso base 2: segundo termo @
  Senao Se (vnTermo = 1) {
    vnResultado = vnAtual;
  } 
  @ Caso recursivo: termos subsequentes @
  Senao {
    fibonacciRecursivo(vnTermo - 1, vnAtual, vnAnterior + vnAtual, vnResultado);
  }
};
```

#### Características Importantes da Recursividade em LSP

1. **Parâmetros de Entrada e Saída**:
   - Use o parâmetro `End` para retornar valores
   - Passe os valores necessários para a próxima chamada recursiva

2. **Condições de Parada**:
   - Sempre defina casos base claros
   - Evite recursão infinita

3. **Chamada Recursiva**:
   - Modifique os parâmetros para se aproximar do caso base
   - Passe os valores atualizados para a próxima chamada

#### Boas Práticas

1. **Eficiência**:
   - Evite recálculos desnecessários
   - Considere usar parâmetros auxiliares para armazenar resultados intermediários

2. **Legibilidade**:
   - Comente claramente os casos base e recursivos
   - Use nomes descritivos para variáveis e parâmetros

3. **Limitações**:
   - Esteja ciente do limite da pilha de chamadas
   - Considere usar abordagens iterativas para problemas muito grandes

#### Exemplo Completo: Sequência de Fibonacci

```lsp
@ Exercício - Sequência de Fibonacci (versão recursiva) @
Definir Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado);
Definir Funcao calcularFibonacci();

@ Função principal @
Definir Numero vnTermos;
Definir Alfa vaTermos;
Definir Alfa vaResultado;
Definir Numero vnContador;
Definir Alfa vaTermo;
Definir Numero vnTermoAtual;

vnTermos = 10; @ Número de termos da sequência @

@ Converter número para alfa @
IntParaAlfa(vnTermos, vaTermos);

@ Montar mensagem inicial @
vaResultado = "Sequência de Fibonacci com " + vaTermos + " termos: ";

calcularFibonacci();

@ Exibir sequência completa @
Mensagem(Retorna, vaResultado);

@ ---FUNÇÕES----@

Funcao calcularFibonacci(); {
  @ Calcular e acumular todos os termos @
  Para (vnContador = 0; vnContador < vnTermos; vnContador++) {
    fibonacciRecursivo(vnContador, 0, 1, vnTermoAtual);
    IntParaAlfa(vnTermoAtual, vaTermo);
    Se (vnContador = 0) {
      vaResultado = vaResultado + vaTermo;
    } Senao {
      vaResultado = vaResultado + ", " + vaTermo;
    }
  }
};

Funcao fibonacciRecursivo(Numero vnTermo, Numero vnAnterior, Numero vnAtual, Numero End vnResultado); {
  Se (vnTermo = 0) {
    vnResultado = vnAnterior;
  } Senao Se (vnTermo = 1) {
    vnResultado = vnAtual;
  } Senao {
    fibonacciRecursivo(vnTermo - 1, vnAtual, vnAnterior + vnAtual, vnResultado);
  }
};
```

Este exemplo demonstra:
- Definição clara de casos base
- Passagem de parâmetros para a próxima chamada recursiva
- Uso do parâmetro `End` para retorno de valores
- Acumulação de resultados em uma string
- Formatação adequada da saída

## Definição de Arrays

Arrays são variáveis com tamanhos definidos que permitem armazenar múltiplos valores do mesmo tipo. Eles são úteis para armazenar coleções de dados de tamanho fixo.

### Declaração de Arrays

Para declarar um array, utilize o comando `Definir` seguido do tipo de dado, o nome da variável e o tamanho do array entre colchetes `[]`.

Exemplo de declaração de arrays:

```lsp
Definir Alfa vaNomes[10];
Definir Numero vnIdades[5];
Definir Data vdDatas[3];
```

### Atribuição de Valores

Os valores podem ser atribuídos aos elementos do array utilizando o índice do elemento entre colchetes `[]`.

Exemplo de atribuição de valores:

```lsp
vaNomes[0] = "João";
vaNomes[1] = "Maria";
vaNomes[2] = "Pedro";

vnIdades[0] = 25;
vnIdades[1] = 30;
vnIdades[2] = 35;

vdDatas[0] = "01/01/2020";
vdDatas[1] = "15/03/2021";
vdDatas[2] = "10/10/2022";
```

### Acesso aos Valores

Os valores dos elementos do array podem ser acessados utilizando o índice do elemento entre colchetes `[]`.

Exemplo de acesso aos valores:

```lsp
Mensagem(Retorna, vaNomes[0]); @ Exibe "João" @
Mensagem(Retorna, vnIdades[1]); @ Exibe 30 @
Mensagem(Retorna, vdDatas[2]); @ Exibe "10/10/2022" @
```

### Iteração sobre Arrays

Os arrays podem ser iterados utilizando estruturas de repetição como `Para` ou `Enquanto`.

Exemplo de iteração sobre arrays:

```lsp
Para (i = 0; i < 3; i++) {
  Mensagem(Retorna, vaNomes[i]);
}

Definir Numero j;
j = 0;
Enquanto (j < 3) {
  Mensagem(Retorna, vnIdades[j]);
  j++;
}
```

### Exemplo Completo

Aqui está um exemplo completo de declaração, atribuição, acesso e iteração sobre arrays:

```lsp
Definir Alfa vaNomes[3];
Definir Numero vnIdades[3];
Definir Data vdDatas[3];

vaNomes[0] = "João";
vaNomes[1] = "Maria";
vaNomes[2] = "Pedro";

vnIdades[0] = 25;
vnIdades[1] = 30;
vnIdades[2] = 35;

vdDatas[0] = "01/01/2020";
vdDatas[1] = "15/03/2021";
vdDatas[2] = "10/10/2022";

Para (i = 0; i < 3; i++) {
  Mensagem(Retorna, vaNomes[i]);
}

Definir Numero j;
j = 0;
Enquanto (j < 3) {
  Mensagem(Retorna, vnIdades[j]);
  j++;
}
```

## Definição de Listas

Sempre que é necessária a customização do sistema (mesmo que seja complexa), as regras podem ser usadas com a vantagem de não precisar recompilar o sistema. Ferramentas como Gerador de Relatórios, Importador e Exportador de Arquivos Texto, por exemplo, também permitem a customização através da regra.

O constante aumento de complexidade dos sistemas gerou a necessidade de mais recursos nas regras. Uma destas necessidades era uma lista dinamicamente alocada, flexível para programador/usuário e que fosse de fácil uso e entendimento.

Tendo conhecimento desta necessidade, foi implementado dentro das regras o recurso conhecido daqui por diante como Lista.

O funcionamento consiste em determinar os campos que a lista usará, preencher a lista com valores e usar estes valores de maneira que atenda às necessidades da lógica implementada pelo programador/usuário.

### Comandos para Definição de Listas

São comandos que determinam o formato da lista. Este formato hoje somente é determinado pelos campos que compõem a lista.

| Comando         | Função                                                                                       |
|-----------------|----------------------------------------------------------------------------------------------|
| tipo Lista      | Serve para determinar o tipo de uma variável que será lista. Nenhum parâmetro adicional será necessário para esta definição. |
| DefinirCampos   | Inicia a fase de adição de campos na lista. Somente podem ser adicionados campos durante este período, ou seja, após a chamada deste comando. |
| EfetivarCampos  | Determinará o fim da adição de campos e informará ao compilador/interpretador que a partir deste ponto a lista será usada efetivamente (receberá valores). Também permitirá ao interpretador criar estruturas internas de controle e manipulação desta lista. |
| AdicionarCampo  | Adiciona os campos. Nesta adição também deve ser informado o tipo e o tamanho se necessário. |

Sintaxe:

```lsp
funcao <lista>.AdicionarCampo(alfa NomeCampo, <tipo> TipoInterno, numero Tamanho);
```

Parâmetros:

- **NomeCampo**: Este parâmetro deve ser uma literal alfanumérica (constante). O nome do campo não deve conter espaços, acentos e nem número como primeiro caractere.
- **TipoInterno**: Deve ser um tipo primitivo interno da regra, ou seja, numero, alfa ou data.
- **Tamanho**: Parâmetro opcional que determina o tamanho do campo. Se informado, somente será aceito para campos alfanuméricos. Neste caso, o campo terá um tamanho limitado. Se não for informado, campos do tipo alfa não terão limite (podem ter valores até o limite de memória). Os outros tipos de campos não são afetados.

### Acesso aos Campos

O acesso aos campos que foram definidos dentro da lista deve ser feito digitando-se o nome da lista, seguido do ponto (.) e o nome do campo. Este nome deverá ser definido previamente através do comando AdicionarCampo.

Caso o nome digitado após o ponto não for um nome de procedimento, função, propriedade ou campo definido na lista, um erro de compilação será gerado.

### Comandos para Manipulação de Registros

Estes comandos permitem adicionar, inserir, gravar, excluir, etc. registros das listas para usar todo o potencial dinâmico do recurso.

| Comando  | Função                                                                                       |
|----------|----------------------------------------------------------------------------------------------|
| Adicionar| É o primeiro comando de manipulação de dados do recurso lista. Ele serve para adicionar valores (agrupados em registros) dentro da lista. Ele cria um registro no final dos registros existentes. Este somente respeitará a ordem de adição se não existirem chaves definidas (será visto mais tarde). |
| Inserir  | Tem a mesma função do comando Adicionar, mas ao invés de adicionar um registro no final dos registros existentes, insere-o na posição atual da lista (apontado internamente e acessível pela propriedade NumReg). |
| Editar   | Visa a atualização de registros. Para tal é necessário posicionar a lista no registro que se deseja alterar. Após isto chama-se o comando Editar e então muda-se os valores desejados. |
| Gravar   | Quando se altera os valores dos campos (após a chamada do comando Adicionar, Inserir ou Editar), pode-se efetivar os dados através do comando Gravar. Grava as informações dentro da lista para posterior recuperação. |
| Cancelar | Ao alterar os valores dos campos, mas por algum motivo os mesmos não devem ser efetivados, utilize o comando Cancelar. Os dados que estão sendo alterados ficam em um registro virtual que não é trabalhado até que seja chamado o comando Gravar ou Cancelar. No caso do comando Cancelar este registro virtual é descartado não alterando o conteúdo da lista. |
| Excluir  | Exclui um registro. Para tal é necessário posicionar a lista no registro que deverá ser excluído e então chamar o comando Excluir. Somente o registro atualmente posicionado será excluído. Para excluir mais registros é necessário chamar o comando mais vezes. |

### Comandos para Posicionamento de Listas

Estes comandos existem para que o programador/usuário possa posicionar o registro da lista e permitir uma maior agilidade no uso do recurso.

| Comando  | Função                                                                                       |
|----------|----------------------------------------------------------------------------------------------|
| Primeiro | Posiciona no primeiro registro que estiver na lista. Note que o primeiro registro pode ser o primeiro adicionado ou o primeiro que respeitar a chave que estiver atualmente selecionada. Exemplo: se existir um campo que for o nome do funcionário e a chave estiver configurada para este campo, o primeiro registro provavelmente será um nome que comece por A. O comando retorna 1 se a lista pôde ser posicionada no primeiro registro e 0 (zero) caso contrário. |
| Ultimo   | Posiciona a lista no último registro. Da mesma forma como o comando Primeiro, o último registro pode ser o último registro adicionado ou o registro que estiver obedecendo a chave. No exemplo anterior (nome do funcionário) o último registro poderia ser um nome que começasse com Z. O comando retorna 1 se a lista pôde ser posicionada no final e 0 (zero) caso contrário. |
| Anterior | O comando Anterior posiciona a lista no registro imediatamente anterior ao registro atual. Se não existir registro anterior, será posicionada em IDA. Segue a mesma lógica de chave do comando Primeiro e Ultimo. Se a lista pôde ser posicionada no registro anterior (que não é o IDA), o comando retorna 1, caso contrário retorna 0 (zero). |
| Próximo  | Posiciona a lista no registro imediatamente posterior ao registro atual. Se não existir registro posterior, será posicionada em FDA. A lógica de chave segue o padrão dos comandos de posicionamento anteriores. Retorna 1 se foi possível posicionar no próximo registro e 0 (zero) caso não tenha conseguido. |

### Comandos para Procura de Registros

Estes comandos auxiliam o programador/usuário na procura de registros dentro da lista através de valores previamente conhecidos.

| Comando    | Função                                                                                       |
|------------|----------------------------------------------------------------------------------------------|
| SetarChave | Coloca a lista em estado de edição de chave para que seja possível a manipulação dos valores da chave. Quando configurados estes valores será possível procurar os registros que possuem a chave informada. Isto será feito através do comando VaiParaChave que será visto a seguir. Apaga os valores que estiverem na chave no momento da chamada. Para manter os valores da chave use o comando EditarChave. |
| EditarChave| Tem o mesmo objetivo do comando SetarChave mas sem apagar os valores de chave. Quando este comando for chamado os valores que estiverem contidos na chave neste momento serão mantidos e ainda assim a lista entrará em modo de edição de chave. Serve para procurar por chaves muito parecidas sem que seja necessário informar todos os valores novamente. |
| VaiParaChave | Procura pelo registro que tiver a chave configurada naquele momento. Exemplo: Consideremos que a chave da lista seja o código de cadastro do funcionário e que o mesmo tenha o valor 10 após a chamada do comando SetarChave. Quando o comando VaiParaChave for chamado a lista será posicionada no primeiro registro onde o número do cadastro do funcionário for 10. Se o registro com esta característica não for encontrado, a lista não será reposicionada. Caso o comando encontre o registro procurado, será retornado 1. Caso contrário será retornado 0 (zero). |

### Comandos para Posicionamento Absoluto

Os comandos a seguir informam e configuram a posição absoluta da lista conforme o número do registro.

| Comando    | Função                                                                                       |
|------------|----------------------------------------------------------------------------------------------|
| NumReg     | Esta propriedade retorna o número do registro (baseado em zero) da posição atual da lista. Se a lista estiver posicionada no quarto registro, o valor retornado será 3. Este número de registro é influenciado pela chave que estiver ativa no momento da obtenção deste valor. Exemplo: Existe um registro na lista que não possui chave definida. O número deste registro é 2. Quando atribuímos uma chave para a lista, outro registro pode ter o número 2 e o registro que antes possuía o número 2 pode ter qualquer outro número, dependendo da chave aplicada. |
| SetaNumReg | Este procedimento tem como objetivo posicionar a lista de maneira absoluta. A posição da lista é a ordem do registro menos 1. A ordem do registro é influenciada pela chave que estiver ativa no momento da chamada. |

### Comandos Diversos de Listas

Os comandos a seguir são de categoria geral, mas são utilizados normalmente com os outros comandos aqui apresentados.

| Comando            | Função                                                                                       |
|--------------------|----------------------------------------------------------------------------------------------|
| Propriedade IDA    | Retorna 1 se a lista estiver em IDA (Início De Arquivo) e 0 (zero) caso contrário. |
| Propriedade FDA    | Retorna 1 se a lista estiver em FDA (Fim De Arquivo) e 0 (zero) caso contrário. |
| Propriedade QtdRegistros | Retorna o número de registros que estão retidos na lista naquele momento. |
| Limpar             | Apaga todos os registros da lista. |
| Procedimento Chave | Este procedimento configura a chave que a lista deverá usar do momento da chamada em diante. Esta chave deve conter os nomes dos campos que estiverem configurados na lista separados por ponto-e-vírgula (;). Caso não se queira chave nenhuma, deve-se configurar este valor com vazio (""). |

### Exemplo

Definição de uma lista:

```lsp
/* Definição das variáveis necessárias para a operação. */
definir lista Lst;

/* Definição de campos dentro da lista declarada acima. */
Lst.DefinirCampos();
Lst.AdicionarCampo("Empresa", numero);
Lst.AdicionarCampo("Tipo", alfa);
Lst.AdicionarCampo("Cadastro", numero);
Lst.AdicionarCampo("Nome", alfa, 100);
Lst.AdicionarCampo("Salario", numero);
Lst.AdicionarCampo("Afastamento", data);
Lst.EfetivarCampos();
```

O campo Nome será do tipo alfanumérico mas tem o seu tamanho limitado. Caso seja atribuído um valor cujo tamanho seja maior que 100, um erro em tempo de execução será mostrado ao usuário.

Neste exemplo são usados os comandos DefinirCampos, AdicionarCampo, EfetivarCampos, além da definição de uma variável do tipo Lista.

### Atribuição de Valores para a Lista

Neste exemplo a lista é preenchida com valores trazidos por um cursor.

```lsp
/* Definição de variáveis utilizadas na regra. */
definir cursor Cur;

/* Determinação da chave. Não influi na inserção de registros. */
Lst.Chave("Nome");

/* Preenchimento da lista com os valores do cursor. */
Cur.SQL "select NumEmp, TipCol, NumCad, NomFun, ValSal, DatAfa from R034FUN";
Cur.AbrirCursor();

enquanto (Cur.Achou) {
  Lst.Adicionar();
  Lst.Empresa = Cur.NumEmp;
  se (Cur.TipCol = 1)
    Lst.Tipo = "Colaborador";
  senao se (Cur.TipCol = 2)
    Lst.Tipo = "Parceiro";
  senao se (Cur.TipCol = 3)
    Lst.Tipo = "Terceiro";
  senao
    Lst.Tipo = "<desconhecido>";
  Lst.Cadastro = Cur.NumCad;
  Lst.Nome = Cur.NomFun;
  Lst.Salario = Cur.ValSal;
  Lst.Afastamento = Cur.DatAfa;
  Lst.Gravar();
  Cur.Proximo();
}
```

Neste exemplo são utilizados os comandos Adicionar, Gravar e Chave. Também são acessados os campos através do nome do mesmo.

### Utilização de Dados de uma Lista

Neste exemplo os dados previamente armazenados na lista estão sendo utilizados para a impressão de seções dentro do gerador de relatórios.

```lsp
definir alfa dsValorTipo;
definir alfa dsValorNome;
definir alfa dsValorEspecial2;
definir alfa dsValorEspecial4;

/* Retirar a chave para imprimir os registros na ordem de inserção. */
Lst.Chave("");
/* Obtém a quantidade de registros atualmente retidos na lista. */
frValorTotalReg = Lst.QtdRegistros;

/* Lista a seção dos dados */
ListaSecao("adCabecalho");

/* Navega por todos os registros da lista obtendo os valores dos campos. */
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Tem = Lst.Proximo();
}

/* Configura a chave do registro para poder proceder com uma procura. */
Lst.Chave("Cadastro;Nome");

/* Configura a chave para a procura do registro com Cadastro 10. */
Lst.SetarChave();
Lst.Cadastro = 10;
se (Lst.VaiParaChave()) {
  frValorEspecial6 = Lst.NumReg;
  frValorEspecial1 = Lst.Empresa;
  dsValorEspecial2 = Lst.Tipo;
  frValorEspecial3 = Lst.Cadastro;
  dsValorEspecial4 = Lst.Nome;
  frValorEspecial5 = Lst.Salario;
  frValorEspecial7 = Lst.Afastamento;
  ListaSecao("adValoresEspeciais");
}

/* Posiciona a lista absolutamente e imprime os dados do registro atual. */
Lst.SetaNumReg(5);
frValorEspecial6 = Lst.NumReg;
frValorEspecial1 = Lst.Empresa;
dsValorEspecial2 = Lst.Tipo;
frValorEspecial3 = Lst.Cadastro;
dsValorEspecial4 = Lst.Nome;
frValorEspecial5 = Lst.Salario;
frValorEspecial7 = Lst.Afastamento;
ListaSecao("adValoresEspeciais");
```

### Exclusão de Dados da Lista

Neste exemplo é mostrado como excluir dados da lista. Neste caso somente serão excluídos os registros cujo campo Salario estiver com um valor menor que 1000.

```lsp
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  se (Lst.Salario < 1000) {
    Lst.Excluir();
    se (Lst.FDA = 1)
      Tem = 0;
    senao
      Tem = 1;
  } senao
    Tem = Lst.Proximo();
}
```

### Algoritmos de Leitura de Dados da Lista

Para a leitura de dados é possível utilizar algumas lógicas. Basta o programador decidir qual a melhor para ele.

#### Utilizando o Retorno das Funções

Este algoritmo utiliza o retorno provido pelas funções de movimentação para identificar o estado da lista. É o mesmo algoritmo apresentado em exemplos anteriores.

```lsp
Tem = Lst.Primeiro();
enquanto (Tem = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Tem = Lst.Proximo();
}
```

#### Utilizando Propriedade Indicadora de Fim de Arquivo (FDA)

Este algoritmo utiliza-se da propriedade FDA para identificar o fim dos registros.

```lsp
Lst.Primeiro();
enquanto (Lst.FDA = 0) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
  Lst.Proximo();
}
```

#### Utilizando Diretamente o Retorno das Funções de Movimentação

Este algoritmo não é usual mas pode ser utilizado. Consiste em colocar a lista no registro virtual IDA e identificar o fim de arquivo através do retorno da função Proximo diretamente. Neste caso o estado de fim de arquivo é obtido apenas uma vez quando da chamada da função Proximo.

```lsp
Lst.Primeiro();
Lst.Anterior();
enquanto (Lst.Proximo() = 1) {
  frValorNumReg = Lst.NumReg;
  frValorEmpresa = Lst.Empresa;
  dsValorTipo = Lst.Tipo;
  frValorCadastro = Lst.Cadastro;
  dsValorNome = Lst.Nome;
  frValorSalario = Lst.Salario;
  frValorAfastamento = Lst.Afastamento;
  ListaSecao("adDetalhe");
}
```

Da mesma forma, estes algoritmos podem ser utilizados começando pelo último registro e subindo até o primeiro. Para isto basta utilizar as funções Ultimo e Anterior.

## Definição de Tabelas

Usado com o comando definir para declarar uma variável do tipo Tabela, com linhas e colunas. Cada coluna é um nome com um tipo específico de informação e as linhas são indexadas de 1 até N.

### Sintaxe

```lsp
Definir Tabela <nome da tabela>[<número de ocorrências>] = { <tipo da variável> <nome da variável>; ... }
```

### Exemplo

Declaração de uma tabela de 12 ocorrências tendo como nome Acumulador, e como variáveis numéricas Media_Mensal e Movimento ocorrendo 31 vezes uma para cada dia do mês e a alfanumérica Nome_Mes com 14 posições:

```lsp
Definir Tabela Acumulador[12] = {
  Numero Media_Mensal;
  Numero Movimento[31];
  Alfa Nome_Mes[14];
};
```

Os caracteres `{` e `}` podem ser substituídos por `Inicio` e `Fim` respectivamente, indicando que as variáveis Media_Mensal e Movimento pertencem ao bloco "Tabela" ao qual tem nome de Acumulador.

### Forma de Acesso à Variável

```lsp
x1 = Acumulador[1].Media_Mensal + 1;
x1 = Acumulador[x2+1].Movimento[x3+1];
Acumulador[1].Nome_Mes = "Janeiro";
Acumulador[2].Nome_Mes = "Fevereiro";
```

Neste exemplo, estamos acessando e manipulando os dados da tabela Acumulador. Cada linha da tabela é indexada de 1 até N, e cada coluna tem um nome específico com um tipo de dado definido.

## Definição de Cursor

### Cursor Simples

Um cursor simples é utilizado para realizar consultas SQL e iterar sobre os resultados. Ele é definido utilizando o comando `Definir` seguido do tipo `Cursor`.

Exemplo de definição de um cursor simples:

```lsp
Definir Cursor curExemplo;
curExemplo.SQL = "SELECT * FROM Tabela";
curExemplo.AbrirCursor();

Enquanto (curExemplo.Achou) {
  Mensagem(Retorna, curExemplo.Campo);
  curExemplo.Proximo();
}

curExemplo.FecharCursor();
```

### Cursor Completo

Um cursor completo é utilizado para realizar consultas SQL mais complexas e iterar sobre os resultados. Ele é definido utilizando o comando `SQL_Criar` e outras funções SQL específicas.

Exemplo de definição de um cursor completo:

```lsp
Definir Alfa xCursor;
Definir Alfa vSql;
Definir Data xData;

vSql = "SELECT * FROM Tabela WHERE Condicao";

SQL_Criar(xCursor);
SQL_UsarSQLSenior2(xCursor, 0);
SQL_UsarAbrangencia(xCursor, 0);
SQL_DefinirComando(xCursor, vSql);
SQL_DefinirInteiro(xCursor, "xNumero", 1);
SQL_DefinirBoleano(xCursor, "xBoleano", 1);
SQL_DefinirFlutuante(xCursor, "xFlutuante", 1.6);
SQL_DefinirData(xCursor, "xData", xData);
SQL_DefinirAlfa(xCursor, "xAlfa", "João da Silva");

SQL_AbrirCursor(xCursor);
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_RetornarAlfa(xCursor, "CAMPO", variavelDestino);
  SQL_Proximo(xCursor);
}
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

### Vantagens e Desvantagens dos Cursores

#### Cursor Simples

**Vantagens:**
- Simplicidade na definição e uso.
- Menor quantidade de funções necessárias.
- Ideal para consultas simples e rápidas.

**Desvantagens:**
- Menos flexível para consultas complexas.
- Não suporta múltiplos parâmetros ou tipos de dados avançados.
- Não permite o uso de determinadas funções SQL.

#### Cursor Completo

**Vantagens:**
- Permite acesso a dados atualizados.
- Permite filtragem dos dados diretamente no banco de dados.
- Suporta operações complexas com múltiplos parâmetros.
- Pode utilizar ou não a sintaxe SQL Senior 2.

**Desvantagens:**
- A performance de resposta depende da rede e do banco de dados.
- Requer mais funções e configurações em comparação ao cursor simples.

## Definição de Funções

É um conjunto de comandos que tem como objetivo calcular um ou mais valores e retorná-los para uso na regra. Havendo uma operação que se repita, pode-se criar a função e chamá-la em cada regra, sem precisar reimplementá-la.

Nota:
Como boa prática, é recomendável que se reserve a regra 001 apenas para implementar funções.

Uma função pode receber parâmetros e retornar valores.

Importante:
Valores alterados dentro da função também serão alterados fora dela.

Os parâmetros definidos para as funções devem obrigatoriamente ser Numéricos. Parâmetros do tipo Alfanuméricos ainda não são suportados por funções definidas nas regras.

### Exemplos de Funções

#### Função Simples

```lsp
Definir Funcao funcaoSimples();

funcaoSimples();

Funcao funcaoSimples() {  
  @ Corpo da Função @
}
```

#### Função com Parâmetro Numérico

```lsp
Definir Funcao adicionarHoras(Numero vnParametro);
Definir Numero vnHoras;

vnHoras = 2;
adicionarHoras(10);
@ o valor de vnHoras será 12 @

Funcao adicionarHoras(Numero vnParametro) {
  vnHoras = vnHoras + vnParametro;
}
```

#### Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro

```lsp
Definir Funcao incrementar(Numero End vnParametro);
Definir Numero vnValor;

vnValor = 1;
incrementar(vnValor);
@ o valor de vnValor será 2 @

incrementar(vnValor);
@ o valor de vnValor será 3 @

incrementar(vnValor);
@ o valor de vnValor será 4 @

Funcao incrementar(Numero End vnParametro) {
  vnParametro = vnParametro + 1;
}
```

#### Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica

```lsp
Definir Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno);
Definir Numero vnHorario;
Definir Numero vnNovoHorario;

vnHorario = 2;
adicionarQuantidadeHoras(vnHorario, 2, vnNovoHorario);
@ o valor de vnNovoHorario será 4 @

Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno) {
  vnRetorno = vnHoraAtual + vnQuantidade;
}
```

### Organização das Funções

Para evitar problemas de execução, as funções devem sempre ficar no final do código. Aqui está um exemplo de como organizar o código corretamente:

```lsp
Definir Funcao funcaoSimples();
Definir Funcao adicionarHoras(Numero vnParametro);
Definir Funcao incrementar(Numero End vnParametro);
Definir Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno);

@ Execução da Função Simples @
funcaoSimples();

@ Execução da Função com Parâmetro Numérico @
Definir Numero vnHoras;
vnHoras = 2;
adicionarHoras(10); @ o valor de vnHoras será 12 @

@ Execução da Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro @
Definir Numero vnValor;
vnValor = 1;
incrementar(vnValor);
@ o valor de vnValor será 2 @

incrementar(vnValor);
@ o valor de vnValor será 3 @

incrementar(vnValor);
@ o valor de vnValor será 4 @

@ Execução da Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica @
Definir Numero vnHorario;
Definir Numero vnNovoHorario;
vnHorario = 2;
adicionarQuantidadeHoras(vnHorario, 2, vnNovoHorario); @ o valor de vnNovoHorario será 4 @

@ ------------------------------------FUNÇÕES----------------------------------@

@ Função Simples @
Funcao funcaoSimples() {  
  @ Corpo da Função @
}

@ Função com Parâmetro Numérico @
Funcao adicionarHoras(Numero vnParametro) { 
  vnHoras = vnHoras + vnParametro; 
}

@ Função com Parâmetro Numérico e Retorno no Mesmo Parâmetro @
Funcao incrementar(Numero End vnParametro) {  
  vnParametro = vnParametro + 1;
}

@ Função com Dois Parâmetros Numéricos e Retorno em uma Variável Específica @
Funcao adicionarQuantidadeHoras(Numero vnHoraAtual, Numero vnQuantidade, Numero End vnRetorno) {
  vnRetorno = vnHoraAtual + vnQuantidade;
}
```

## Retorno para Aplicação

Usado apenas no gerador de relatórios, para alterar o valor de um campo tipo Descrição ou Numérico. O valor passado para ValRet ou ValStr será impresso no lugar do valor original do campo. Essas palavras reservadas devem ser utilizadas em conjunto com o comando `Cancel(2);`.

### ValRet

A função `ValRet` é utilizada para retornar valores numéricos para a aplicação.

Exemplo de uso do `ValRet`:

```lsp
ValRet = 10;
Cancel(2);
```

### ValStr

A função `ValStr` é utilizada para retornar valores alfanuméricos para a aplicação.

Exemplo de uso do `ValStr`:

```lsp
ValStr = "Texto de Retorno";
Cancel(2);
```

## Funções Gerais

As funções gerais na LSP são utilizadas para realizar operações comuns, como manipulação de strings, datas e números.

| Nome                        | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| AlfaParaInt                 | Converte um número armazenado como Alfa e o retorna como um tipo Número.  |
| ArqExiste                   | Verifica se um arquivo físico existe no local especificado.               |
| AtualizaBarraProgresso      | Atualiza as mensagens apresentadas na tela da barra de progresso.         |
| CaracterParaAlfa            | Converte um caracter (que fica armazenado pelo código ASCII) para o valor Alfanumérico correspondente. |
| CodData                     | Possibilita a composição de uma data, montando-a através de dia, mês e ano.|
| ConverteCodificacaoString   | Esta função converte a codificação de um texto para o formato definido pelo usuário. |
| ConverteMascara             | Esta função converte um valor de entrada (numérico, data, hora ou cadeia de caracteres), para o tipo de dado cadeia de caracteres. |
| ConverteParaMaiusculo       | Converte o conteúdo de uma variável do tipo Alfa para maiúsculo.          |
| ConverteParaMinusculo       | Converte o conteúdo de uma variável do tipo Alfa para minúsculo.          |
| ConverteTexto               | Substitui os caracteres especiais informados no texto de acordo com a codificação do padrão informada, retorna em uma nova variável o texto convertido. |
| CopiarAlfa                  | Esta função copia parte do conteúdo de uma variável/campo alfanumérico para a variável alfanumérica Retorno. |
| CriarArquivoTemporario      | Cria um arquivo temporário de nome aleatório e único prefixado com o valor do parâmetro prefixo. |
| DataHoje                    | Retorna a data atual do sistema operacional.                              |
| DataHora                    | Retorna data e hora atual.                                                |
| DecodData                   | Permite a separação de uma data em dia, mês e ano para que os dados possam ser usados separadamente. |
| DeletarAlfa                 | Esta função apaga uma determinada quantidade de caracteres de uma variável/campo a partir da posição informada. |
| Desencriptar                | Função para descriptografar uma cadeia de caracteres.                     |
| Dividir                     | Função disponível para dividir um valor por outro.                        |
| Encriptar                   | Criptografa a cadeia de caracteres.                                       |
| ExcluirArquivoTemporario    | Exclui um arquivo criado pela função CriarArquivoTemporario.              |
| ExecProg                    | Permite a execução de aplicativos durante a execução de regras.           |
| FinalizaBarraProgresso      | Finaliza a tela de barra de progresso.                                    |
| FormatarData                | Formata a data.                                                           |
| GeraHash                    | Retorna um Hash do texto informado.                                       |
| GerarNonce                  | Gera o valor do campo Nonce, um número aleatório.                         |
| GerarPwdDigest              | Gera o Digest da senha, a partir do Nonce, Data e senha, em formato base64.|
| GeraSenha                   | Retorna uma sequência de caracteres alfanuméricos aleatoriamente.         |
| GeraToken                   | Retorna um token criptografado.                                           |
| HoraParaMinuto              | Converte em minutos os valores que representam hora e minuto.             |
| IniciaBarraProgresso        | Inicia a barra de progresso utilizada para mostrar ao usuário o andamento de um processo mais extenso. |
| IntParaAlfa                 | Converte um número para formato alfanumérico, desprezando as casas decimais.|
| LerPosicaoAlfa              | Identifica qual caracter está em determinada posição do campo/variável de origem. |
| LinhasArquivo               | Leitura da quantidade de linhas existentes em um determinado arquivo.     |
| ListaItem                   | Retorna o valor de um item de uma lista de valores concatenados por um caracter separador. |
| ListaQuantidade             | Retorna a quantidade de itens de uma lista de valores concatenados por um caracter separador em um texto. |
| Mensagem                    | Apresenta a mensagem em tela de acordo com a parametrização do tipo de retorno e da mensagem que será visualizada. |
| ObtemIdiomaAtivo            | Retorna o código do idioma utilizado pelo usuário.                        |
| ObterVersaoSistema          | Esta função retorna a versão do sistema.                                  |
| OcultaBarraProgressoRelatorio | Oculta a barra de progresso padrão durante a execução de relatórios.    |
| PosicaoAlfa                 | Procura por uma parte de texto dentro de um campo/variável do tipo Alfa, retornando a posição em que o texto inicia. |
| RemoveExpressoesProibidas   | Não permite que campos de relatórios/regras aceitem algum tipo de script. |
| RestoDivisao                | Retorna o resto da divisão de um número por outro.                        |
| RetornaValorCFG             | Responsável por retornar para a regra o valor de uma determinada chave da Central de Configuração Senior que está sendo utilizada pelo sistema. |
| TamanhoAlfa                 | Verifica o tamanho do campo Alfa especificado em Origem.                  |
| TrocaString                 | Procura por um trecho específico dentro de um texto e o substitui, retornando um novo texto. |
| Truncar                     | Trunca um número para inteiro, removendo a parte fracionária do número.   |
| VerificaAbaAtiva            | Verifica, pela descrição passada por parâmetro, se essa é a descrição da aba ativa. |
| VrfAbrA                     | Verifica se um determinado valor está contido em uma abrangência especificada. |
| VrfAbrN                     | Verifica se um determinado valor numérico está contido em uma abrangência especificada. |
| sleep                       | Pausa a execução do código por X milesegundos |

Para mais detalhes sobre cada função, consulte a @documentação da Senior.

## Funções SQL

As funções a seguir podem ser utilizadas para manipulação de comandos SQL e o resultado dos comandos (cursores) em regras. A partir destas funções podem ser executados comandos DML (INSERT, UPDATE, DELETE) e também comandos SELECT que retornam cursores que poderão ser manipulados também.

| Nome                | Descrição                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------|
| SQL_AbrirCursor     | Função que abre o cursor (depois de informado o comando SQL a ser utilizado, que é definido na função SQL_DefinirComando). |
| SQL_BOF             | Função que retorna a informação se o cursor está na posição inicial (antes do primeiro registro: posição BOF). |
| SQL_Criar           | A partir de uma variável criada como alfa, é criado um cursor para trabalhar com informações da base de dados. |
| SQL_DefinirAlfa     | Função que define um valor do tipo alfa para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBlob     | Função que define um valor do tipo alfa (que representa o arquivo blob) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirBoleano  | Função que define um valor do tipo boolean (Número 1 para verdadeiro e 0 para falso) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirComando  | Função que aplica o comando SQL para o cursor passado como parâmetro. |
| SQL_DefinirData     | Função que define um valor do tipo data ou date para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirFlutuante| Função que define um valor do tipo flutuante ou float (Fracionado Ex: 1,5) para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_DefinirInteiro  | Função que define um valor do tipo inteiro para o parâmetro dentro do comando SQL inserido na função SQL_DefinirComando. |
| SQL_Destruir        | Função que elimina um cursor e deve ser chamada quando o cursor não for mais utilizado. |
| SQL_EOF             | Função que retorna se o cursor está na posição final (depois do último registro chamada de posição EOF). |
| SQL_FecharCursor    | Função que fecha a pesquisa sendo feita pelo cursor. |
| SQL_Proximo         | Função que posiciona o cursor no próximo registro. |
| SQL_RetornarAlfa    | Função que retorna um valor alfa de um campo do registro do cursor. |
| SQL_RetornarBlob    | Função que retorna um valor alfa de um campo do registro do cursor. |
| SQL_RetornarBoleano | Função que retorna um número que representa um valor boolean, 1 para verdadeiro e 0 (zero) para falso, de um campo do tipo boolean do cursor. |
| SQL_RetornarData    | Função que retorna um valor do tipo data de um campo do registro do cursor. |
| SQL_RetornarFlutuante| Função que retorna um valor flutuante (fracionado, por exemplo 1,5) de um campo do registro do cursor. |
| SQL_RetornarInteiro | Função que retorna um valor inteiro de um campo do registro do cursor. |
| SQL_RetornarSeNulo  | Função que retorna se campo do registro do cursor é nulo. |
| SQL_UsarAbrangencia | Função que informa ao cursor se é para utilizar abrangência de usuários ou não. |
| SQL_UsarSQLSenior2  | Função que informa se o comando a ser definido para o cursor utiliza a sintaxe de linguagem Senior ou a sintaxe nativa (SQL Nativa: linguagem originada da base de dados utilizada, ex: Oracle, SQL server...etc). |


### SQL Senior 2

A linguagem Senior SQL 2 pode ser utilizada nas regras dos geradores de informação (gerador de relatórios e consultas), regras de cálculo (regras avulsas executadas diretamente pelo sistema) e importador/exportador de arquivos texto. Esta linguagem é um padrão adotado pela Senior para que os comandos SQL possam ser escritos em um formato padrão que permita um melhor aprendizado e uma melhor tradução para os bancos de dados suportados pelos sistemas da Senior.

#### Ativação da Linguagem

- **Gerador de Relatórios**: Menu principal do gerador > Diversos > Usar Senior SQL 2.
- **Importador/Exportador de Arquivos Texto**: Página Definições > Usar Senior SQL 2.
- **Gerador de Consultas**: Tela principal de definição de modelos > Senior SQL 2.
- **Regras**: Editor de regras > Compilar > Usar Senior SQL 2 ou Ctrl + F12.

#### Restrições

- **Funções de Agregação**: Funções como SUM, COUNT, MAX não podem ser usadas dentro da cláusula SELECT.
- **Comandos Nativos do Banco de Dados**: Comandos como TO_DATE ou CONVERT devem ser substituídos por comandos da linguagem Senior SQL 2.
- **JOIN e UNION**: Não têm garantias de funcionamento dentro das regras.

### Exemplos

#### Utilização de INSERT

```lsp
Definir Alfa xCursor;
Definir Alfa xBlob;

SQL_Criar(xCursor);

@ Insere um novo registro na tabela de intervalos. @
SQL_DefinirComando(xCursor, "INSERT INTO R006INT VALUES (9999, 'Exemplo de intervalo')");
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

#### Utilização de SELECT

```lsp
Definir Alfa xCursor;

@ Cria o cursor. @
SQL_Criar(xCursor);

@ Define um comando para poder carregar as informações no Cursor. @
SQL_DefinirComando(xCursor, "SELECT R034FUN.CODFIL FROM R034FUN WHERE R034FUN.CODFIL = 1");

@ Abre o cursor para utilização. @
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

@ Fecha o cursor depois de utilizar. @
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

#### Utilização de UPDATE

```lsp
Definir Alfa xCursor;
Definir Alfa xBlob;

SQL_Criar(xCursor);

@ Atualiza as informações na base de dados através do comando UPDATE. @
SQL_DefinirComando(xCursor, "UPDATE R034FOT SET FOTEMP = :xBlob WHERE NUMEMP = 9999");

@ Abre o arquivo para a leitura (Indicado pelo 2º parâmetro). @
xArquivo = Abrir("C:/Teste.jpg", Ler);

@ Lê o arquivo que foi aberto acima, e o atribui à variável xBlob (em binário). @
Ler(xArquivo, xBlob, 9999999);

SQL_DefinirBlob(xCursor, "xBlob", xBlob);
SQL_AbrirCursor(xCursor);

/* Todas as operações referentes à base de dados
   serão feitas entre abrirCursor e fecharCursor. */

SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

### Passagem de Parâmetros

A passagem de parâmetros para dentro de um cursor pode ser feita utilizando `__inserir` ou `SQL_Definir<tipo_variavel>` e passando com `:` para dentro da query, em vez de concatenar um valor na Query.

O `:` é utilizado para indicar que se trata de um parâmetro que será substituído por um valor específico antes da execução do comando SQL. Isso é comum em consultas parametrizadas para evitar a concatenação direta de valores nas strings SQL, o que pode ajudar a prevenir injeções de SQL, melhorar a legibilidade e manutenção do código, pois não é necessário converter variáveis para alfa para concatenar na query. O ideal é sempre utilizar passagem de parâmetro e evitar concatenar variáveis na query.

#### Exemplo com `__inserir`

```lsp
Definir Cursor C;
Definir Numero vnCodEmp;
Definir Numero vnCodFil;
Definir Alfa vaOrderBy;

vnCodEmp = 1;
vnCodFil = 6;
vaOrderBy = "ORDER BY CODFIL";

C.SQL "SELECT NumEmp, TipCol, NumCad, NomFun, ValSal FROM R034FUN WHERE CodEmp = __inserir(:vnCodEmp) and CodFil = __inserir(:vnCodFil) __inserir(:vaOrderBy)";

C.AbrirCursor();
se (C.Achou) {
  // ...existing code...
}
C.FecharCursor();
```

#### Exemplo com `SQL_Definir<tipo_variavel>`

```lsp
Definir Alfa xCursor;
Definir Numero xNumero;

SQL_Criar(xCursor);
SQL_DefinirComando(xCursor, "SELECT * FROM Tabela WHERE Campo = :xNumero");
SQL_DefinirInteiro(xCursor, "xNumero", 123);

SQL_AbrirCursor(xCursor);
Enquanto (SQL_EOF(xCursor) = 0) {
  SQL_Proximo(xCursor);
}
SQL_FecharCursor(xCursor);
SQL_Destruir(xCursor);
```

# Manipulação de Arquivos

## Visão Geral
A LSP oferece um conjunto de funções para manipulação de arquivos texto e binários. Estas funções permitem operações de leitura, escrita e gerenciamento de arquivos no sistema.

## Funções Principais

### Abrir
Abre um arquivo para leitura ou escrita.

**Sintaxe**: `numero Abrir(Alfa NomeArq, TModeAbert ModoAbertura);`

**Parâmetros**:
- `NomeArq`: Caminho do arquivo (ex: "C:\\Pasta\\arquivo.txt")
- `ModoAbertura`: Modo de abertura do arquivo
  - `Ler`: Leitura binária
  - `Gravar`: Escrita binária
  - `Lernl`: Leitura em modo texto
  - `Gravarnl`: Escrita em modo texto

**Retorno**: Manipulador do arquivo (número)

**Exemplo**:
```lsp
Definir numero vnArquivo;
vnArquivo = Abrir("C:\\Logs\\sistema.log", Lernl);
```

### Fechar
Fecha um arquivo previamente aberto.

**Sintaxe**: `Fechar(numero ManArquivo);`

**Parâmetro**:
- `ManArquivo`: Manipulador do arquivo retornado pela função Abrir

**Exemplo**:
```lsp
Fechar(vnArquivo);
```

### Ler
Lê bytes de um arquivo binário.

**Sintaxe**: `numero Ler(numero ManArquivo, alfa end Var, numero NumBytes);`

**Parâmetros**:
- `ManArquivo`: Manipulador do arquivo
- `Var`: Variável que receberá os dados lidos
- `NumBytes`: Quantidade de bytes a serem lidos

**Retorno**: Número de bytes lidos

**Exemplo**:
```lsp
Definir Alfa vaConteudo;
Definir numero vnBytesLidos;
vnBytesLidos = Ler(vnArquivo, vaConteudo, 1024);
```

### LerNL
Lê uma linha de um arquivo texto.

**Sintaxe**: `numero Lernl(numero ManArquivo, alfa end Var);`

**Parâmetros**:
- `ManArquivo`: Manipulador do arquivo
- `Var`: Variável que receberá a linha lida

**Retorno**: 1 se leu com sucesso, 0 se chegou ao final do arquivo

**Exemplo**:
```lsp
Definir Alfa vaLinha;
Definir numero vnLeu;
vnLeu = Lernl(vnArquivo, vaLinha);
```

### Gravar
Escreve bytes em um arquivo binário.

**Sintaxe**: `numero Gravar(numero ManArquivo, alfa Var, numero NumBytes);`

**Parâmetros**:
- `ManArquivo`: Manipulador do arquivo
- `Var`: Dados a serem gravados
- `NumBytes`: Quantidade de bytes a serem gravados

**Retorno**: Número de bytes gravados

**Exemplo**:
```lsp
Definir Alfa vaDados;
vaDados = "Conteúdo do arquivo";
Gravar(vnArquivo, vaDados, 1);
```

### GravarNL
Grava uma linha em um arquivo texto.

**Sintaxe**: `Gravarnl(numero ManArquivo, alfa Var);`

**Parâmetros**:
- `ManArquivo`: Manipulador do arquivo
- `Var`: Linha a ser gravada

**Exemplo**:
```lsp
Gravarnl(vnArquivo, "Nova linha de texto");
```

### GravarNLEOL
Grava uma linha em um arquivo texto com opção de quebra de linha.

**Sintaxe**: `numero GravarNLEOL(numero ManArquivo, alfa Var, logico UseEOL);`

**Parâmetros**:
- `ManArquivo`: Manipulador do arquivo
- `Var`: Linha a ser gravada
- `UseEOL`: Se verdadeiro, adiciona quebra de linha

**Exemplo**:
```lsp
GravarNLEOL(vnArquivo, "Linha com quebra", 1);
```

## Exemplos Práticos

### 1. Leitura de Arquivo Texto
```lsp
Definir Alfa vaCaminho;
Definir Alfa vaConteudo;
Definir Alfa vaLinha;
Definir numero vnArquivo;
Definir numero vnLeu;

vaCaminho = "C:\\Logs\\sistema.log";
vnArquivo = Abrir(vaCaminho, Lernl);
vnLeu = 1;

Enquanto (vnLeu = 1) {
    vnLeu = Lernl(vnArquivo, vaLinha);
    Se (vnLeu = 1) {
        vaConteudo = vaConteudo + vaLinha;
    }
}
Fechar(vnArquivo);
```

### 2. Escrita em Arquivo de Log
```lsp
Definir Alfa vaCaminho;
Definir Alfa vaMensagem;
Definir Alfa vaData;
Definir numero vnArquivo;

vaCaminho = "C:\\Logs\\sistema.log";
vaMensagem = "Operação realizada com sucesso";
DataHora(vnDataHora);
FormatarData(vnDataHora, "DD/MM/YYYY - HH:mm:ss", vaData);

vnArquivo = Abrir(vaCaminho, Gravarnl);
GravarNLEOL(vnArquivo, vaData + ": " + vaMensagem, 1);
Fechar(vnArquivo);
```

## Observações Importantes

1. **Quebra de Linha**:
   - No Windows, use CRLF (#13#10)
   - Exemplo de configuração:
   ```lsp
   Definir Alfa vaEnter;
   Definir Alfa vaNovaLinha;
   RetornaAscii(13, vaEnter);
   RetornaAscii(10, vaNovaLinha);
   ```

2. **Verificação de Existência**:
   - Use a função `ArqExiste` antes de manipular o arquivo
   ```lsp
   Se (ArqExiste(vaCaminho) = 1) {
       @ Arquivo existe @
   }
   ```

3. **Tratamento de Erros**:
   - Sempre feche o arquivo após o uso
   - Verifique o retorno das funções de leitura/escrita
   - Trate casos de arquivo inexistente

4. **Boas Práticas**:
   - Use caminhos absolutos
   - Escape corretamente as barras invertidas
   - Mantenha o arquivo aberto pelo menor tempo possível
   - Sempre feche o arquivo após o uso

## Chamada de Web Service

O Editor de Regras dispõe de um conjunto de funções para que seja possível a atribuição e manipulação dos parâmetros de um web service, bem como a sua execução. Para isto é necessário declarar uma variável identificando o serviço que se deseja executar.

**Sintaxe:**

```lsp
@ Definir idProvedor.idServico.idPorta VarName; @

Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula;
```

A variável informada é a que será utilizada para acessar os parâmetros, funções da porta, ler, fazer atribuições e comparações com os parâmetros.

**Importante:**

Para que não ocorra conflito nas chamadas de web service, caso existam regras que utilizem o mesmo web service, a variável declarada deve ser uma diferente das já existentes.

**Exemplo:**

```lsp
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula2;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula3;
Definir interno.com.senior.g5.rh.fp.calculoFolha.Calcular vCalcula4;
```

### Modos de Execução

Os modos de execução de web service via regra LSP são tratados por numeração na regra, conforme abaixo:

1. Local
2. Síncrono
3. Assíncrono

**Importante:**

Não é possível utilizar o modo de execução Agendado em regras LSP, pois não é possível informar a periodicidade na regra.

O parâmetro `ModoExecucao = 1 (Local)` deve ser utilizado apenas em regras que serão executadas em instâncias de web services. Ou seja, esse parâmetro não deve ser usado nas seguintes formas de acesso: Cliente-Servidor, BrowserAccess, WindowsAccess, Web 5.0 e processos automáticos.

### WS-Security

Permite a integração de sistemas que utilizam web services terceiros com autenticação WS-Security. Com isto, as chamadas destes web services, do tipo SOAP, permitem a inclusão de informações de segurança no cabeçalho e assim, a sua integração.

A customização desta chamada é realizada a partir de um parâmetro na regra LSP: `WSSeguranca`, que receberá um XML e posteriormente será repassado para o cabeçalho do envelope SOAP:

```lsp
Webservice.WSSeguranca = "XML_Segurança";
```

### Autenticação

A autenticação de web services é feita, por padrão, através dos parâmetros `usuario`, ou `user`, e `senha`, ou `password`. Quando não informado, a autenticação é feita através dos valores do usuário do sistema.

Caso desejar ignorar os parâmetros, acesse a Central de Configurações Senior e insira a chave `com.senior.middleware.webservices.use_implicit_params_login` com o valor `false`.

## Chamada HTTP

A LSP permite a chamada de endpoints HTTP utilizando comandos específicos para enviar e receber dados.

### Funções para Requisições HTTP

Funções que possibilitam a execução de requisições HTTP, oferecendo suporte à utilização de servidor proxy e requisições sobre SSL, permitindo o acesso a sites da web que utilizem HTTPs.

| Nome                          | Descrição                                                                 |
|-------------------------------|---------------------------------------------------------------------------|
| HttpAdicionaExcecaoProxy      | Adiciona o endereço passado no parâmetro Endereço na lista de exceções de proxy. |
| HttpAlteraAutenticacaoProxy   | Faz o inverso da função HttpLeAutenticacaoProxy, ou seja, altera os valores ao invés de ler. |
| HttpAlteraCabecalhoRequisicao | Altera valores de cabeçalhos HTTP que serão enviados junto com a requisição. |
| HttpAlteraCodifCaracPadrao    | Altera a codificação de caracteres que é usado por padrão nas respostas do servidor. |
| HttpAlteraConfiguracaoProxy   | Faz o inverso da função HttpLeConfiguracaoProxy, ou seja, altera os valores ao invés de ler. |
| HttpAlteraConfiguracaoSSL     | Faz o inverso da função HttpLeConfiguracaoSSL, ou seja, altera o valor ao invés de ler. |
| HttpAlteraMostrarProgresso    | Faz o inverso da função HttpLeMostrarProgresso, ou seja, altera o valor ao invés de ler. |
| HttpAlteraRedirecionamento    | Especifica se as requisições realizadas devem tratar os redirecionamentos retornados pelo servidor destino. |
| HttpDelete                    | Executa uma requisição HTTP usando o método DELETE. |
| HttpDeleteBody                | Executa uma requisição HTTP usando o método DELETE (com parâmetro Body). |
| HttpDesabilitaErroResposta    | Desabilita a geração automática de erros de execução. |
| HttpDesabilitarCookies        | Desabilita o recurso de manter os cookies ao utilizar requisições HTTP em regras LSP. |
| HttpDesabilitaSNI             | Desabilita o SNI (Server Name Indication) na requisição HTTP. |
| HttpDownload                  | Funciona da mesma maneira que a função HttpGet, porém o retorno não é na memória, mas sim em um arquivo salvo diretamente em disco. |
| HttpExcluiExcecaoProxy        | Exclui da lista de exceções de proxy o endereço do índice passado como parâmetro em Índice, contado a partir do 0 (zero). |
| HttpGet                       | Executa uma requisição HTTP (inclusive HTTPS) de acordo com a URL passada como parâmetro e salva a resposta da requisição, por exemplo, uma página HTML, no parâmetro de retorno HTML. |
| HttpHabilitaErroResposta      | Habilita a geração automática de erros de execução. |
| HttpHabilitarCookies          | Habilita o recurso de manter os cookies ao utilizar requisições HTTP. |
| HttpHabilitaSNI               | Habilita o SNI (Server Name Indication) na requisição HTTP. |
| HttpLeAutenticacaoProxy       | Faz a leitura e retorna os valores do usuário e senha de autenticação no servidor proxy. |
| HttpLeCabecalhoResposta       | Consulta os valores associados à cabeçalhos de respostas das requisições. |
| HttpLeCodigoResposta          | Consulta o código de resposta de uma requisição enviada ao servidor. |
| HttpLeConfiguracaoProxy       | Faz a leitura do valor das propriedades Utilizar servidor proxy, Servidor, Porta e Utilizar autenticação por usuário do objeto HTTP e os retorna nos parâmetros UsarProxy, Servidor, Porta e AutPorUsu, respectivamente. |
| HttpLeConfiguracaoSSL         | Faz a leitura da propriedade Utilizar SSL do objeto HTTP e retorna o valor em SSL. |
| HttpLeContadorExcecoesProxy   | Neste contexto, exceções de proxy são endereços (URLs) que podem ser acessadas sem passar pelo servidor proxy. |
| HttpLeExcecaoProxy            | Retorna no parâmetro Endereço o endereço cadastrado na lista de exceções de proxy no índice passado como parâmetro em Índice, contado a partir do 0 (zero). |
| HttpLeMostrarProgresso        | Faz a leitura da propriedade Exibir progresso de download do objeto HTTP e retorna o valor em Mostrar. |
| HttpLimpaExcecoesProxy        | Exclui todos os endereços cadastrados na lista de exceções de proxy. |
| HttpNormalizaRetorno          | Aplica a normalização de texto para caracteres de combinação na resposta da requisição HTTP. |
| HttpObjeto                    | Esta função retorna um objeto HTTP inicializado com as configurações definidas na tela de Configurações de Internet da Central de Configurações. |
| HttpPatch                     | Realiza uma chamada de verbo PATCH do HTTP. |
| HttpPost                      | Executa uma requisição HTTP usando o método POST. |
| HttpPut                       | Executa uma requisição HTTP usando o método PUT. |
| HttpSetAttachment             | Adiciona arquivo no corpo da requisição HTTP. |
| HttpSetaTimeout               | Atribui um timeout (tempo de espera) para uma requisição HTTP. |

Para mais detalhes sobre cada função, consulte a @documentação da Senior.

### Exemplos de Código

#### Exemplo 1: Busca o CEP na API VIA CEP

```lsp
Funcao buscarCepApi(Numero vnCepApi) {
  Definir Alfa vaCepApi;
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaCodRes;
  Definir Alfa vaMsgUsu;
  Definir Numero vnCodRes;

  @Tratamento de Variáveis@
  vaURL = "https://viacep.com.br/ws/__NUMCEP__/json/"; @URL do ViaCEP@
  vaJSON = ""; @Objeto de Retorno da Requisição@
  vnCodRes = 0; @Cód. HTTP Response@

  ConverteMascara(1, vnCepApi, vaCepApi, "99999999");
  TrocaString(vaURL, "__NUMCEP__", vaCepApi);

  @Cria Objeto HTTP@
  HttpObjeto(vaHTTP);

  @Desabilita Erro Padrão, evita que mensagens de erros HTTP 4XX/5XX gerem Exceptions em tela ao usuário@
  HttpDesabilitaErroResposta(vaHTTP);

  @Altera os Cabeçalhos da Requisição@
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json;charset=utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Encoding", "gzip, deflate, br");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Charset", "utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json;charset=utf-8");
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

  @Efetua a Requisição@
  HttpGet(vaHTTP, vaURL, vaJSON);

  @Verifica Cód. HTTP Response@
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  @Se a resposta foi "OK", extrai os dados do JSON@
  Se ((vnCodRes >= 200) e (vnCodRes <= 204)) {
    @Logradouro@
    ValorElementoJson(vaJSON, "", "logradouro", vaLogradouro);

    @Complemento@
    ValorElementoJson(vaJSON, "", "complemento", vaComplemento);

    @Bairro@
    ValorElementoJson(vaJSON, "", "bairro", vaBairro);

    @Cidade@
    ValorElementoJson(vaJSON, "", "localidade", vaCidadeCep);

    @Estado@
    ValorElementoJson(vaJSON, "", "uf", vaEstadoCep);

    @IBGE@
    ValorElementoJson(vaJSON, "", "ibge", vaIbge);
  }

  @Tratamento de Erro@
  Se ((vnCodRes < 200) ou (vnCodRes >= 300)) {
    @Tratamento de Variáveis@
    IntParaAlfa(vnCodRes, vaCodRes);

    @Mensagem@
    vaMsgUsu = "HTTP [" + vaCodRes + "]: Verifique os parâmetros da requisição";
    Mensagem(Retorna, vaMsgUsu);
  }
}
```

#### Exemplo 2: Busca a Cidade na API IBGE

```lsp
Funcao buscarCidadeApi(Numero vnCidApi) {
  Definir Alfa vaCidApi;
  Definir Alfa vaHTTP;
  Definir Alfa vaURL;
  Definir Alfa vaJSON;
  Definir Alfa vaCodRes;
  Definir Alfa vaMsgUsu;
  Definir Numero vnCodRes;

  vdDatSis = DatSis;

  @Tratamento de Variáveis@
  vaURL = "https://servicodados.ibge.gov.br/api/v1/localidades/municipios/__NUMCID__?view=nivelado"; @URL do IBGE@
  vaJSON = ""; @Objeto de Retorno da Requisição@
  vnCodRes = 0; @Cód. HTTP Response@

  ConverteMascara(1, vnCidApi, vaCidApi, "9999999");
  TrocaString(vaURL, "__NUMCID__", vaCidApi);

  @Cria Objeto HTTP@
  HttpObjeto(vaHTTP);

  @Desabilita Erro Padrão, evita que mensagens de erros HTTP 4XX/5XX gerem Exceptions em tela ao usuário@
  HttpDesabilitaErroResposta(vaHTTP);

  @Altera os Cabeçalhos da Requisição@
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept", "application/json;charset=utf-8");
  @HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Encoding", "gzip, deflate, br");@
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Accept-Charset", "utf-8");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Cache-Control", "no-cache");
  HttpAlteraCabecalhoRequisicao(vaHTTP, "Content-Type", "application/json;charset=utf-8");
  HttpAlteraCodifCaracPadrao(vaHTTP, "utf-8");

  @Efetua a Requisição@
  HttpGet(vaHTTP, vaURL, vaJSON);

  @Verifica Cód. HTTP Response@
  HttpLeCodigoResposta(vaHTTP, vnCodRes);

  @Se a resposta foi "OK", extrai os dados do JSON@
  Se ((vnCodRes >= 200) e (vnCodRes <= 204)) {
    @Cidade@
    ValorElementoJson(vaJSON, "", "municipio-nome", vaCidadeRai);

    @Estado@
    ValorElementoJson(vaJSON, "", "UF-sigla", vaEstadoRai);
  }

  @Tratamento de Erro@
  Se ((vnCodRes < 200) ou (vnCodRes >= 300)) {
    @Tratamento de Variáveis@
    IntParaAlfa(vnCodRes, vaCodRes);

    @Mensagem@
    vaMsgUsu = "HTTP [" + vaCodRes + "]: Verifique os parâmetros da requisição";
    Mensagem(Retorna, vaMsgUsu);
  }
}
```
