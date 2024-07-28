# Avaliação Front-End (Vue/Prime)

## Objetivo
Esta avaliação tem como objetivo a criação de uma página pública de inscrição para atletas em eventos, onde os mesmos podem escolher qual(is) eventos desejam participar.
Caso o usuário deseje se inscrever o sistema deverá fazer o controle do fluxo de seleção do evento, preenchimento do formulário da inscrição com seleção das modalidades desejadas no determinado evento, e de acordo com as modalidades selecionadas, fazer o cálculo do valor total da inscrição e bem como a confirmação da inscrição.

## Projeto/Repositório (GitHub)
- O link para clone do repositório base com os pacotes instalados está disponível no link [GitHub](https://github.com/ludhriq/avaliacao).
- O projeto está configurado com os seguintes aspectos/pacotes:
  - Javascript
  - ViteJs (Servidor Local)
  - [VueJS](https://vuejs.org) v3.4.29 (SFC .vue)
  - [PrimeVue](https://primevue.org) v4.0.2 (Biblioteca de componentes feito com VueJs para UI/UX)
  - [TailwindCSS](https://tailwindcss.com/) v3.4.7 (Utilização `opcional`)
  - [DayJs](https://day.js.org) (Manipulação de datas)
  - [VeeValidate](https://vee-validate.logaretm.com/v4/) (Formulário)
  - [Yup](https://github.com/jquense/yup) (Validação)
- Os dados fictícios das entidades para confecção das telas estão no arquivo `"dados.js"`
- Instalar pacotes: `npm install`
- Iniciar aplicação: `npm run dev`

## Lista de Tarefas
### 1) Listagem de Eventos (Página Principal):
- Criar a listagem de eventos, que também vai atuar como página principal, onde caso o usuário clique em um dos eventos, o sistema deverá direcioná-lo para a página de Inscrição do Evento [2]. </br>
- Os eventos precisam ser listados em ordem decrescente pelo campo `inicioEm`.
- Os eventos precisam incluir a foto de capa.
- Os eventos precisam indicar se estão em fase de inscrição ou não de acordo com os campos `inicioInscricaoEm` / `terminoTerminoEm`.
- Caso o evento já tenha ocorrido ou esteja fora do período de inscrição, ele ainda precisa ser listado, porém de uma forma na qual não seja possível realizar inscrições.
- **Recomendação**: Utilizar o componente `DataTable` do primevue.

### 2) Inscrição do Evento:
- Na tela de inscrição de um evento, deverá ser criado um formulário, onde o usuário deverá preencher os campos: `nome`, `cpf`, `email`, `dataNascimento` bem como uma seleção de `modalidades` que deseja participar (As modalidades já estão pré definidas no objeto deste evento). Os campos deverão ser validados de acordo. </br>
- O usuário poderá se inscrever em quantas modalidades quiser, deverá ser visível para ele os valores da inscrição por modalidade. </br>
Após selecionar as modalidades desejadas, o usuário deverá clicar no botão `"Confirmar Inscrição"` e ser redirecionado para a Tela de Confirmação [3].
- **Recomendação**: Utilizar componentes de formulário do primevue, a validação do formulário com o `vee-validate` (No componente home do projeto existe um exemplo básico de validação de formulário).

### 3) Confirmação da Inscrição:
- Nesta etapa, o usuário deverá ver o resumo de todas as informações preenchidas por ele na inscrição, com opção de retornar para a tela anterior [2] e fazer modificações. 
- Abaixo do resumo da inscrição deverá existir um botão `"Gerar Código de Pagamento"`. Após clicar no botão uma nova seção será incluída na tela simulando a geração de um QrCode para pagamento via PIX (Imagem do QrCode fixa disponibilizada no projeto).
- Deverá ser exibida uma mensagem a respeito do pagamento abaixo do `QrCode` com os seguintes dizeres: `"Após o pagamento via PIX, a inscrição pode levar até 1 hora para ser confirmada."`.
- Após o pagamento fictício por parte do usuário, ele deverá clicar no botão `"Confirmar Pagamento"`, após clicar, uma modal deverá ser exibida com um agradecimento pela realização da inscrição além de uma mensagem fixa com os dizeres `"Um email será enviado para ${email} com a confirmação de sua inscrição."`.
- Na modal deverá ser incluído um botão para navegar de volta para a listagem de eventos [1].
- **Recomendação**: Utilizar o componente `Dialog` do primevue.

## Considerações finais
- As telas precisam ser adaptadas para interfaces `Mobile` e `Desktop`.
- Após o término da avaliação, o candidato deverá fazer um commit de volta ao repositório do GitHub.
- As cores, tamanhos, estilo, ou qualquer outro aspecto visual/adicional que não tenha sido informado `explicitamente` no requisito poderá ser desenvolvido de forma livre pelo candidato, para justamente dar liberdade e avaliar sua criatividade.
- O resultado da avaliação vai levar em conta os seguintes critérios gerais: Estrutura/Organização do Código, Estrutura Visual/Criatividade (UI/UX) e Conhecimento específico em VueJS.  

