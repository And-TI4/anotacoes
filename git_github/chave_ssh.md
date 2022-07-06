## Criando uma chave SSH

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

Será solicitada a senha criada quando foi gerada a chave SSH.