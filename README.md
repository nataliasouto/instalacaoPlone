### CMS PLONE 5 – Instalação e Demonstração

Esta é uma documentação não oficial de instalação do Plone no windows 10
Você pode ler a documentação oficial em [docs.plone.org](https://docs.plone.org/) .

É importante lembrar que você pode instalar o Plone em seu computador independente do sistema operacional utilizado. Para isso basta acessar o site do Plone, fazer o download do instalador do Plone para seu sistema operacional.

Se você ainda não sabe o que é o Plone, dá uma olhada no artigo que fiz [Conheça o PLONE: O CMS em Python](http://viladosilicio.com.br/conheca-o-plone-o-cms-em-python/).

### Requisitos
### Python 2.7.x x86-64 MSI Installer
Baixe e instale o [Python 2.7.14](https://www.python.org/downloads/windows/).
Atenção: ative “Incluir pyton.exe no Path” como na imagem abaixo:

![python-installer](https://user-images.githubusercontent.com/31136465/72561503-1eb35b80-3888-11ea-8945-9d81fd921484.png)

### Microsoft Visual C ++ Compiler para Python 2.7
Instale o compilador [MSVC ++ para Python 2.7](https://www.microsoft.com/en-us/download/details.aspx?id=44266). Não há opções nesta instalação.

### Plone Unified Installer
Acesse [plone.org](https://plone.org/) e baixe a última versão do instalador unificado (Unified Installer) do Plone.
O instalador unificado é instalado e operado através do Prompt de Comando do Windows.

Atualmente está na versão [release 5.1.4 ](https://plone.org/download/releases/5.1.4).

### Instalação
Após preparar seu ambiente e baixar a versão unificada do plone, abra o prompt de comando do Windows. Mude o seu diretório atual para o local de download e use **_`tar`_** para descompactar o download:

```
CD Download
tar xf Plone-5.1.x-UnifiedInstaller.tgz
```
ou caso a versão seja uma release:

```
CD Download
tar xf Plone-5.1.x-UnifiedInstaller-r1.tgz
```

_*Substitua o x pelo número de versão. Isso você vai encontrar no arquivo baixado do plone._

Altere seu diretório atual para o diretório do arquivo descompactado e execute a rotina de lote de instalação do Windows:

```
cd Plone-5.1.x-UnifiedInstaller
./windows_install.bat standalone --password=admin
```

### Resultados
Espere que o instalador leve um tempo considerável para ser executado, com muito poucas mensagens após o início da compilação. No final da instalação, espere uma mensagem como:

```
Plone instalado com sucesso em \ Users \ steve \ Plone \ zinstance
Consulte \ Usuários \ steve \ Plone \ zinstance \ README.html
para instruções de inicialização.
 
Use as informações da conta abaixo para entrar na interface de gerenciamento do Zope
A conta tem privilégios de 'Gerente' completos.
 
  Nome de usuário: admin
  Senha: admin
 
Essa conta é criada quando o banco de dados de objetos é inicializado. Se você mudar
a senha depois (o que você deve!), você precisará usar a nova senha.
 
Use essa conta apenas para criar sites e usuários iniciais do Plone. Não use isso
para login ou manutenção de rotina.
```

### Iniciando o Serviço do Plone
Após o término da instalação, o Plone ainda não está em execução. Se faz necessário iniciá-lo.
Primeiro acesse a pasta do plone que foi gerada no seu disco C, normalmente neste caminho:

**C:\Users\SEU_USUÁRIO\Plone**

Agora acesse a pasta zinstance dentro da pasta Plone e execute o seguinte comando para inicializar no modo de primeiro plano(possivelmente você verá erros no console, esse é um modo de desenvolvimento):

`./bin/plonectl fg
`

O Python irá pedir permissões para acessar as redes públicas e privadas. Aceite normalmente.

Agora, acesse em seu browser o endereço [http://localhost:8080/](http://localhost:8080) e a seguinte página deve ser exibida:

![Plone-localhost](https://user-images.githubusercontent.com/31136465/72561999-2cb5ac00-3889-11ea-850d-754fb102e727.png)

### Suporte
Se você estiver tendo problemas informe no espaço comunitário em: [community.plone.org/c/documentation](https://community.plone.org/c/documentation).


