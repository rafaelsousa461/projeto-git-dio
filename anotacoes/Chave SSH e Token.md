#Adicionar uma nova chave SSH à sua conta do GitHub

	##Gerando Chave SSh
	
	 - Abra Git Bash.
	 - Cole o texto abaixo, substituindo o endereço de e-mail pelo seu GitHub.
			$ ssh-keygen -t ed25519 -C "your_email@example.com"
			
	 - Quando aparecer a solicitação "Enter a file in which to save the key" (Insira um arquivo no qual salvar a chave),
		presssione Enter. O local padrão do arquivo será aceito.
	 - Digite uma frase secreta segura no prompt
	 
	 ## Adicionar sua chave SSH ao ssh-agent

	 - Certifique-se de que o ssh-agent está em execução. Você pode usar as instruções "Lançamento automático do ssh-agent" em "Trabalhando com palavras-chave SSH" ou iniciá-lo manualmente:
		# start the ssh-agent in the background
		$ eval "$(ssh-agent -s)"
		> Agent pid 59566
	 - Sua chave SSH privada ao ssh-agent. Se você criou sua chave com um nome diferente ou se estiver adicionando uma chave existente com um nome diferente, substitua id_ed25519 no comando pelo nome do arquivo de chave privada.
		$ ssh-add ~/.ssh/id_ed25519
	 - Adicione a chave SSH à sua conta em GitHub. 