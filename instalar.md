# Instalar o Python em seu SO

## Python no Linux
O Python está instalado no Linux. Para saber qual a versão utilizada em sua distribuição Linux abra o terminal  e digite
```sh
$ python -V
Python 2.7.12
```
Tente ainda por meio desse comando
```sh
$ python3 -V
Python 3.5.2
```
Caso a versão 3 não esteja instalada execute no terminal o camando abaixo para instalar o Python 3.5 e algumas ferramentas de desenvolvimento.
```sh
sudo apt update # atualiza os repositórios do seu SO (opcional)
sudo apt install python3 idle-python3.5 python3-pip -y
```

# Virtualenv
A vantagem em preparar um ambiente por meio do Virtualenv é que pode-se criar projetos com versões especificas de programa sem que estes entrem em conflito.
Para instalar o Virtualenv use o pip (índice de pacotes do Python), conforme o comando abaixo:
```sh
  sudo pip3 install virtualenv
```
para criar seu ambiente com o Virtualenv. Para isso, vá para a pasta que deseja trabalhar e abra o terminal. Em seguida execute o comando abaixo:
```sh
  virtualenv -p python3.5 <nomeDaPasta>
```
É recomendada a indicação do nome da versão do Python que se deseja utilizar, ex.:
```sh
  virtualenv -p python3.5 ./mundoSenai/python3.5
```

Caso seja necessário usar as variáveis glonais do sistema:
```sh
  virtualenv -p python3.5 --system-site-packages <nomeDaPasta>
```
Ou, se não for necessário usar as variáveis glonais do sistema:
```sh
  virtualenv -p python3.5 --no-site-packages <nomeDaPasta>
```
Para ativar seu Virtualenv
```sh
  source <nomeDaPasta>/bin/activate
```
Para desativar seu Virtualenv
```sh
  deactivate
```
Para remover seu Virtualenv
```sh
  revirtualenv <nomeDaPasta>
```
Agora inicie seu Virtualenv para instalar o Django

# Django no Linux
Para começar a utilizar o django é necessário instalá-lo em sua máquina. Para instalar o Django no Linux digite o comando abaixo, no terminal, por meio do pip, em seu Virtualenv:
```sh
  pip3 install -U pip
  sudo pip3 install django==1.9
```
Uma dica: o pip3 permite fazermos uma lista de potes que temos em um certo computador para porteriormente isntalá-los em outro computador:
```sh
  pip3 freeze > requeriments.txt
```
Instalar os requisitos e dependência no outro computador
```sh
  pip3 install -r requeriments.txt
```
