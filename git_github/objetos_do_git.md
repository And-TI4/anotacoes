## Objetos do Git

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
