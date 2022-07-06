## Git

**Hash**

​	É o código do tipo sha1 gerado com base no conteúdo dos arquivos.

**Gerando um código do tipo SHA1 para encriptação e identificação de um arquivo.**

​	``openssl sha1 texto.txt``



**Principais objetos do Git**

- Blobs

- Trees

- Commits



**Blob (Bolha)**

- Local onde são armazenados a hash e algumas outras informações que se relacionam com os arquivos.

**Gerando um código SHA1 incluindo as informações geradas pelo objeto blob.**

​	`` echo 'conteúdo' | git hash-objec –stdin ``

**Gerando um código sha1 sem incluir as informações geradas pela blob**.

​	``echo -e 'blob 9\0conteudo' | openssl sha1``



**Tree  (Árvore)**

- Aponta para as blobs e para outras árvores.

- Contém informações sobre os arquivos que ela aponta.

- Também possui um código sha1 próprio.



**Commit**

- Aponta para uma árvore e aponta para o último commit realizado antes dele.
- Contém informações do autor e uma mensagem contendo uma descrição para que seja dado sentido as ações ou modificações feitas.
- Armazena data e hora que os arquivos foram criados.



**Criando uma chave SSH utilizando o Git Bash**

​	``ssh-keygen -t ed25519 -C and4@ymail.com``

​	Depois será solicitado a criação de uma senha.

**Exibir chave SSH**

​	Entrar na pasta .ssh:	

​	``cd /c/Users/TI\Quatro/.ssh/``

​	Digitar ls para exibir os arquivos dentro da pasta e depois o comando abaixo para exibir a chave:

​	``cat id_ed25519.pub``

##### Adicionar sua chave SSH ao ssh-agent

​	``eval $(ssh-agent -s)``

Depois que iniciar o ssh-agent, ir para a pasta .ssd e passar a chave privada com o comando abaixo:

​	``ssh-add id_ed25519``