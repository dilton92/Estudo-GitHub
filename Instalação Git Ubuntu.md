# Estudos GitHub

## Instalação no Ubuntu: 

*sudo apt install git*

## Desinstalação no Ubuntu:

### Desinstalar git
Para desinstalar somente git do Ubuntu 14.04 (Trusty Tahr) execute no terminal:

*sudo apt-get remove git*

### Desinstalar git e os pacotes dependentes
Para desinstalar o pacote git e quaisquer outros pacotes dependentes que não sejam mais necessários do Ubuntu:

*sudo apt-get remove --auto-remove git*

### Expurgar git
Se você também deseja limpar as configurações e/ou dados de git do Ubuntu Trusty então use este comando:

*sudo apt-get purge git*

### Para limpar as configurações e/ou arquivos de dados do git e de seus pacotes dependentes do Ubuntu Trusty execute:

*sudo apt-get purge --auto-remove git*

Caso não consiga com algum desses comandos acima, existe outra solução:  
_sudo find /usr/local -depth -iname 'git*' -exec rm -rf {} \;_  (Isso apaga todos os arquivos relacionados ao git)
