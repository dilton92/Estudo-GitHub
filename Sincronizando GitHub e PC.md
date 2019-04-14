## Sincronizando GitHub e PC

Existem duas maneiras de utilizar o GitHub: a primeira é acessando o site e por meio dele
criar os projetos e arquivos que desejar. Essa forma de acesso é chamada de Acesso HTTPS. A
segunda maneira é "sincronizando" o seu PC com o repositório, dessa forma não precisamos entrar
no site toda vez que quisermos salvar nossos arquivos no GitHub. Para realizarmos a segunda forma
de acesso precisamos de uma chave SSH.

#### Verificando chaves SSH existentes

Se voce já instalou e utilizou o Git na sua máquina, provavelmente já possui uma ou várias chaves
SSH. Para verificar se já possui uma chave, utilize o seguinte comando:
```ls -al ~/.ssh```. 
Caso a mensagem: **"Arquivo ou diretório não encontrado"** apareça para você, é sinal que o Git ainda
não foi utilizado em sua máquina. Então será necessário criar uma nova chave.

#### Criando uma nova chave SSH

1. Para criar essa chave utilize o seguinte comando:

   ```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```.

   Note que o ```-C``` é um comando para adicionar um comentário. Esse comentário pode ser algo que te 
   ajude a lembrar o motivo que o levou a criar essa chave ou apenas o seu e-mail.

2. Em seguida aparecerá uma mensagem que diz:

   ```> Generating public/private rsa key pair.```

3. Será solicitado que você crie um arquivo onde a chave deverá ser guardada. O caminho pode ser alterado.

   ```Enter a file in which to save the key (/home/nome_do_pc/.ssh/id_rsa): [Press enter]```

   Por padrão, o Git cria um arquivo oculto que pode ter um dos seguintes nomes:
   * id_dsa.pub.
   * id_ecdsa.pub.
   * id_ed25519.pub.
   * id_rsa.pub.

4. Será solicitado que você crie uma senha para sua chave SSH. Essa é uma camada extra de segurança e não
é passo obrigatório na geração da chave, porém é recomendado que gere a senha

   ```
   > Enter passphrase (empty for no passphrase): [Type a passphrase]
   > Enter same passphrase again: [Type passphrase again]
   ```

### Adicionando a chave SSH à sua conta GitHub


Se você criou sua chave sem senha, basta abrir o arquivo onde a chave foi salva e copiar o conteúdo
para adicioná-lo à sua conta do GitHub. Você deve localizar a pasta oculta, usando o seguinte comando:
```ls ~/.ssh```, abrir o arquivo no seu editor de texto favorito e copiar o conteúdo. Outra maneira de
copiar a chave é utlilizar o [```xclip```]().

Caso você tenha gerado a chave com senha, então será necessário [adicioná-la ao ```ssh-agent```]().

1. No canto superior direito de qualquer página, clique na foto do seu perfil e clique em ***Settings***.
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/userbar.png "userbar")
   
2. Na barra lateral de configurações do usuário, clique em ***SSH and GPG keys***.
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/sidebar-ssh-keys.png "sidebar-ssh-keys")
   
3. Clique em ***New SSH key*** ou ***Add SSH key***.
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/ssh-add-ssh-key.png "ssh-add")
   
4. No campo "Title", adicione um rótulo descritivo para a nova chave. Por exemplo, se você estiver usando
um Mac pessoal, poderá chamar essa chave de "Personal MacBook Air".
   
5. Cole sua chave no campo "Key".
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/key-paste.png "key-paste")
   
6. Clique em ***Add SSH key***.
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/add-key.png "add-key")
   
7. Se solicitado, confirme sua senha do GitHub.
   ![alt text](https://github.com/dilton92/Estudo-GitHub/blob/master/confirm.png "confirm")
