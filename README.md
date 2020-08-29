# Como instalar o Reactive Native Cli no Windows
### Primeiro Passo: Instalar o Chocolatey!
- No menu iniciar busque por `Windows PowerShell`, clique então com o botão direito sobre e selecione a opção 'Executar como administrado'.
- O Windows pedirá consentimento sobre a execução como administrador, então clique em `Sim`.
- No terminal PowerShell execute os seguintes comandos:
> Get-ExecutionPolicy


> Set-ExecutionPolicy Bypass -Scope Process -Force


> Iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
- Se ao executar o comando 'Get-ExecutionPolicy' for retornado `Restricted` execute um dos seguintes comandos para corrigir e então feche e abra novamente o terminal e volte a executar desde o primeiro comando.

> Set-ExecutionPolicy AllSigned 

e utilize a opção [A], ou

> Set-ExecutionPolicy Bypass -Scope Process.
- Se tudo ocorrer bem, execute *choco* ou *choco -?* e verifique se o terminal irá retornar a sua versão do Chocolatey

### Segundo Passo: Instalação do Node
- Ainde dentro do PowerShell, execute o segundo comando e mantenha o PowerShell aberto para executar todos os próximos comandos:
> choco install -y nodejs.install

### Terceiro Passo: Instalação do Python2
- Execute o comando:
> choco install -y python2

### Quarto Passo: Instalação do Java SDK 8
- Execute o comando:
> choco install -y jdk8

### Quinto Passo: Instalação do Android Studio
- Para fazer o download do Android Studio (Clique Aqui)[https://developer.android.com/studio/index.html]
- Após terminado o download, inicie a instalação e se atente ao se deparar com a tela **Tipo de Instalação** ou **Install Type** que será dado como opção durante a instalação. Nesta tela você terá duas opções: a 'Padrão ou Standard' e a opção 'Custom ou Customizada', nela você deverá optar por **Custom**.
- Em Custom você deverá garantir que as seguintes opções estejam selecionadas:
> [x] Android SDK


> [-] Android SDK Platform


> [x] API xx: Android...


> [x] Performance


> [x] Android Virtual Device

- Ainda nessa mesma tela, você deverá personalizar a opção na parte inferior chamada **Android SDK Location**, nela coloque um caminho personalizado, que não possua caracteres especiais. *Sugestão* utilize o caminho: "C:\Android". Você deverá também **copiar** esta localização para que a utilizemos mais tarde.

### Sexto Passo: Configurações do Sistema
- No menu do Windos busque por:
> Configurações Avançadas do Sistema
- Na tela que for apresentada, na própria aba Avançado, clique na opção "Variáveis de Ambiente...".
- Em Variáveis de Ambiente haverá Variáveis de Usuário e Variáveis do Sistema. Iremos optar por por **Variáveis do Sistema** e nela clicaremos em **Novo**.
- Será aberto uma pequena janela com o título Nova Variável do Sistema, nela iremos preencher:
"Nome da variavél" com o valor:
> ANDROID_HOME
"Valor da Variável" com o valor copiado anteriormente (*Android SDK Location*):
> C:\Android
- Dê OK, e você voltará para a tela de Variáveis do Sistema, agora você deverá encontrar a variavel PATH dentro das Variáveis do Sistema, ao acha-la, clique duas vezes sobre ela.
- Dentro da edição da variável de ambiente iremos adicionar uma nova variável, para isso clique em **NOVO**.
- Adicione então o valor que você copiou mais o prefixo "\platform-tools", como o exemplo abaixo e então clique em OK.
> C:\Android\platform-tools

### Setimo Passo: Concluindo a Instalação
- Abra novamente o PowerShell como administrador e execute o segundo comando:
> adb
- Do comando acima, será retornado no PowerShell o Andorid Debug Bridge Version.
- Por fim, iremos então executar a instalação do Cli nativo do react. Para isso execute:
> npm install -g react-native-cli
- Feito isso, concluímos a instalação do ambiente e cli.

###### by: urnauzao
