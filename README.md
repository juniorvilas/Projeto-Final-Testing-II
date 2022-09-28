# Projeto-Final-Testing-II
Curso: Cetified Tech Developer - DH
Data: 27/09/2022
Projeto em dupla: [Carlindo Junior](https://github.com/juniorvilas) e [Larissa Nunes](https://github.com/Larissa-Nunes)

Enunciado: [link](https://docs.google.com/document/d/1JfxtFWFwAibaAxgFtn-coSRMgc3LUYiYfzD4HEV1i90/edit)

## **Objetivo**
Criar um projeto completo de Testes Automatizados utilizando Java e Selenium, com Suítes, Tags, e Reports, validando também uma API RestAssured. *E pra finalizar faremos uma integração com Jenkins (opcional)*

**Site a ser testado:** [Para Bank](https://parabank.parasoft.com/parabank/index.htm) : 

**Pré-condições:** Abrir o site

**Título do Caso de Teste:** Processo de registro, abertura de nova conta, visão geral das contas, transferir fundos, atividade da conta, para todas as etapas de Testes Front-end

**Testes Front-end:**

 * **Registro**
    1. Clicar em <Register>
    2. Preencher o formulário de registro com os dados exigidos
    3. Clicar em <Register> novamente 
    4. Verificar se o texto “Your account was created successfully. You are now logged in.” está visível na tela

* **Abertura de nova conta**
    1. Clicar em <Open New Account>
    2. Em tipo de conta “What type of Account would you like to open?” selecionar a opção <SAVINGS>
    3. Clicar am <Open New Account> 
    4. Verificar se o texto “Congratulations, your account is now open.” está visível na tela
    
 
 * **Visão geral das contas**
    1. Clicar em <Accounts Overview>
    2. Verificar se o texto “*Balance includes deposits that may be subject to holds” está visível na tela

* **Transferir Fundos**
    1. Clicar em <Transfer Funds>
    2. Verificar se o texto “Transfer Funds” está visível na tela
    3. No campo <Amount: $> preencher o valor a ser transferido
    4. No campo <From account #> selecionar uma conta
    5. No campo <to account #> selecionar uma conta diferente da conta anterior
    6. Clicar em <Transfer>
    7. Verificar se o texto “Transfer Complete!” está visível na tela

* **Atividades da conta (todos os meses)**
    1. Clicar <Accounts Overview>
    2. Verificar se o texto “*Balance includes deposits that may be subject to holds” está visível na tela
    3. Clicar am em uma conta na coluna <Account> 
    4. Verificar se o texto “Account Details” está visível na tela
    5. Em “Account Activity” clicar em <Activity Period:> e selecionar “All”
    6. Em “Account Activity” clicar em <Type:> e selecionar “All”
    7. Clicar em <Go>

**Testes back-end API Rest:**
* **Validação de status code 200 para todas as etapas de Testes Front-end**
    1. Registro URL: [link](https://parabank.parasoft.com/parabank/register.htm)
    2. Abertura de nova conta URL: [link](https://parabank.parasoft.com/parabank/services_proxy/bank/createAccount?customerId=12545&newAccountType=1&fromAccountId=xxxxx)
    3. Visão geral das contas URL: [link](https://parabank.parasoft.com/parabank/overview.htm)
    4. Transferir Fundos URL: [link](https://parabank.parasoft.com/parabank/services_proxy/bank/transfer?fromAccountId=13566&toAccountId=13677&amount=xxxxx)
    5. Atividades da conta (todos od meses) URL: [link](https://parabank.parasoft.com/parabank/services_proxy/bank/accounts/13566/transactions/month/All/type/All)

**Integração com Jenkins:**
* **Adicione o seu código a um repositório Github para integrá-lo ao Jenkins e criar o Job Pipeline**
    1. Crie seu repositório Github aberto (não privado)
    2. Crie um Job Pipeline (Pipeline Script from SCM)


**Dica:**

Não é necessário informar dados verdadeiros nos formulários durante o teste.
Podemos utilizar, por exemplo,  um gerador de dados: https://generatedata.com/
Não se esqueça de criar o arquivo “jenkinsfile” na sua estrutura de código para configurá-lo no Jenkins (Script Path).


