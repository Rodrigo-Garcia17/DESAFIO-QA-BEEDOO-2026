<<<<<<< HEAD
# DESAFIO QA – Beedoo 2026

Autor: Rodrigo Garcia da Silva
Cargo pretendido: Analista da Qualidade Jr - Tecnologia/Software

---

# 1. Análise inicial da aplicação

A aplicação analisada possui como objetivo permitir o **cadastro e a listagem de cursos**.

O sistema permite que o usuário:

- Cadastre novos cursos
- Visualize cursos cadastrados
- Exclua cursos da listagem

Durante a exploração inicial da aplicação foi possível identificar que o fluxo principal envolve o preenchimento de um formulário de cadastro contendo as seguintes informações:

- Nome do curso
- Descrição
- Instrutor
- URL da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso (Online ou Presencial)

Dependendo do tipo selecionado:

Online → campo de link de inscrição  
Presencial → campo de endereço

Após o cadastro, os cursos são exibidos em uma página de **listagem**, onde aparecem em formato de cards contendo algumas das informações registradas.

Também existe a funcionalidade de **exclusão de cursos**, acessível através de um botão presente em cada card da listagem.

---

# 2. Decisões tomadas para criação dos testes

Após a análise inicial da aplicação, foram definidos alguns pontos prioritários para a criação dos cenários de teste.

Os testes foram elaborados considerando principalmente:

- Verificação do fluxo principal de cadastro de cursos
- Validação de campos obrigatórios
- Regras de negócio relacionadas às datas
- Validação do número de vagas
- Consistência das informações exibidas na listagem
- Funcionamento da funcionalidade de exclusão de cursos

Também foram incluídos cenários negativos e testes de limite para verificar como o sistema se comporta diante de dados inválidos ou incompletos.

Essa abordagem permitiu avaliar não apenas o funcionamento esperado do sistema, mas também sua robustez diante de entradas incorretas.

---

# 3. Explicação do raciocínio durante a análise

A análise da aplicação foi realizada inicialmente por meio de **exploração manual das funcionalidades disponíveis**.

Primeiramente foram identificados os principais fluxos da aplicação:

- Cadastro de cursos
- Listagem de cursos
- Exclusão de cursos

A partir desses fluxos foram definidos cenários de teste positivos para validar o funcionamento esperado do sistema.

Em seguida, foram criados cenários negativos e testes de validação de campos, considerando possíveis comportamentos inesperados como:

- campos obrigatórios não preenchidos
- valores inválidos
- inconsistência entre datas
- valores extremos no número de vagas

Durante a execução dos testes também foram realizados **testes exploratórios**, que permitiram identificar falhas adicionais relacionadas à validação de dados e à exibição das informações na listagem.

---

# 4. Estratégia de testes

A estratégia utilizada incluiu:

- Testes de fluxo principal
- Testes de cenários negativos
- Testes de validação de campos
- Testes de valores limite
- Testes exploratórios

Os cenários foram documentados utilizando o formato **Gherkin (Dado / Quando / Então)**.

---

# 5. Cenários e casos de teste

Os cenários e casos de teste foram documentados em uma planilha no Google Sheets.

Planilha de testes:

https://docs.google.com/spreadsheets/d/1h0CmTy8pAHCJZ76Ytqs0I71BnCkd36_Y/edit?usp=sharing

---

# 6. Resumo da execução dos testes

Durante a execução foram criados e executados **13 cenários de teste**.

| Caso de Teste | Descrição | Status |
|---|---|---|
CT01 | Cadastro de curso com dados válidos | Passou |
CT02 | Cadastro com todos os campos em branco | Falhou |
CT03 | Cadastro sem nome do curso | Falhou |
CT04 | Data final menor que data inicial | Falhou |
CT05 | Número de vagas inválido | Falhou |
CT06 | URL de imagem inválida | Falhou |
CT07 | Campos preenchidos apenas com espaços | Falhou |
CT08 | Verificação da listagem de cursos | Falhou |
CT09 | Exclusão de curso | Falhou |
CT10 | Número de vagas negativo | Falhou |
CT11 | Número de vagas extremamente alto | Falhou |
CT12 | Cadastro de múltiplos cursos | Passou |
CT13 | Número de vagas igual a zero | Falhou |

---

# 7. Bugs encontrados

Durante a execução dos testes foram identificados os seguintes problemas:

| ID | Problema |
|----|----------|
BUG01 | Formato de data inconsistente |
BUG02 | Falta de validação de campos obrigatórios |
BUG03 | Sistema permite cadastro com data final menor que data inicial |
BUG04 | Sistema permite cadastro com URL de imagem inválida |
BUG05 | Listagem não exibe algumas informações cadastradas |
BUG06 | Exclusão de curso não remove o item da listagem |
BUG07 | Sistema permite cadastro com número de vagas negativo |
BUG08 | Sistema permite número de vagas extremamente alto |
BUG09 | Sistema permite cadastro com número de vagas igual a zero |

---

# 8. Evidências da execução dos testes

As evidências da execução dos testes estão disponíveis na pasta compartilhada no Google Drive:

https://drive.google.com/drive/folders/1eUGlmIKGWSbmehEUMc-HPAjPsofAiV8E

A pasta contém:

- Prints das telas utilizados durante a execução dos cenários de teste
- Vídeo demonstrando o BUG06 – exclusão de curso não remove o item da listagem
- Vídeo demonstrando a listagem de cursos após a execução dos testes

---

# 9. Análise de risco

Durante os testes foram identificadas diversas falhas relacionadas principalmente à **validação de dados de entrada**.

Os principais riscos para o sistema são:

- Cadastro de cursos com informações incompletas
- Inconsistência de dados exibidos na listagem
- Falhas nas regras de negócio relacionadas ao número de vagas
- Falha na funcionalidade de exclusão de cursos

Esses problemas podem impactar diretamente:

- confiabilidade dos dados cadastrados
- experiência do usuário
- integridade das informações exibidas no sistema

---

# 10. Conclusão

A aplicação apresenta funcionamento básico adequado para o fluxo principal de cadastro e listagem de cursos.

Entretanto, foram identificadas diversas falhas relacionadas principalmente à validação de dados e consistência das informações exibidas.

Recomenda-se a implementação de validações adicionais para garantir maior confiabilidade e integridade das informações cadastradas no sistema.
=======
# DESAFIO-QA-BEEDOO-2026
Desafio técnico para vaga de Analista de Qualidade de Software Júnior – análise da aplicação, cenários de teste, execução e registro de bugs.
>>>>>>> da8ed8112db6a88fe64862647c6f84d0fa256a15
