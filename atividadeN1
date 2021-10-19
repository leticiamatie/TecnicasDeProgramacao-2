inscritos=[]
cadastrados={}
i=0

menu = True
opcao = 0
systemRun = True

while systemRun == True:
	#menu
	while menu == True:
		print("Selecione uma opção:")
		print("-----------------------------")
		print("[1] - Cadastrar novo usuário")
		print("[2] - Exibir usuários cadastrados")
		print("[3] - Buscar usuário")
		print("[4] - Remover usuário")
		print("[5] - Alterar usuário")
		opcao = int(input(""))
		print("")
		if opcao <1 or opcao>5:
			print("Opção inválida!")
		else:
			break

	#cadastra os usuarios
	def cadastraUsuario():

		print("Cadastro de usuário:")
		print("-----------------------------")
		nome = input("Nome: ")
		email = input("E-mail: ")
		cadastrados[nome] = {
      "nome": nome,
      "email": email
    }

		

		print("Usuário Cadastrado com sucesso!")
		print("")


	#exibe os  usuarios
	def exibeInscrito():
		for nome, email in cadastrados.items():
			print("Nome:",nome)
			emailres = str(email["email"])
			print("Email:",emailres)
			print("")

	#exibe em ordem alfabética
	def exibeAlfab():
		for nome, email in sorted(cadastrados.items()):
			print("Nome:",nome)
			emailres = str(email["email"])
			print("Email:",emailres)
			print("")

	#encontra pelo nome
	def encontraNome(procurado):
		encontrado_nome= 0
		for nome,email in cadastrados.items():
			if procurado == nome:
				encontrado_nome = nome
				break
		if encontrado_nome !=0:
			print("Nome:",encontrado_nome)
			emailres = str(email["email"])
			print("Email:",emailres)
			print("")
			print("")
		elif encontrado_nome == 0:
			print("Esse usuário não esta inscrito")
			print("")
	
	def deletaNome(procurado):
		for nome,email in cadastrados.items():
			emailres = str(email["email"])
			encontrado_email = 0
			if procurado == emailres:
				encontrado_email = emailres
				break
		if encontrado_email != 0:
			cadastrados.pop(nome)
			print("Removido com sucesso!")
			print("")
		else:
			print("Usuário não encontrado")
			print("")
			
			
	def alteraUsuario():
		procurado = input("Digite o email do usuário a ser alterado: ")
		print("")
		res = 1
		for nome,email in cadastrados.items():
			emailres = str(email["email"])
			encontrado_email = 0
			if procurado == emailres:
				encontrado_email = emailres
				break
		if encontrado_email != 0:	
			cadastrados.pop(nome)
			nome = input("Novo nome: ")
			email = input("Novo E-mail: ")
			cadastrados[nome] = {
    		"nome": nome,
    		"email": email
    		}
			print("Cadastro alterado com sucesso!")
			print("")
		else:
			print("Esse usuário não existe!")
			print("")

				




	#opção 1
	if opcao == 1:
		cadastraUsuario()
	
	#opção 2
	if opcao == 2:
		print("Selecione um metodo de organização:")
		print("[1] - ordem de cadastro")
		print("[2] - ordem alfabética")
		tipo = int(input(""))

		if tipo == 1:
			print("Usuários ativos:")
			print("-----------------------------")
			exibeInscrito()
			print("-----------------------------")
			print("")
			print("")
		elif tipo == 2:
			print("Usuários ativos:")
			print("-----------------------------")
			exibeAlfab()
			print("-----------------------------")
			print("")
			print("")
		else:
			print("Opção inválida!")

#opção 3
    if opcao == 3:
        print("Buscar por nome:")
        print("-----------------------------")
        nome_procurado = input("Digite o nome a ser encontrado: ")
        encontraNome(nome_procurado)

    #opção 4
    if opcao == 4:
        print("Excluir usuário pelo E-mail:")
        print("-----------------------------")
        procurado = input("Digite o E-mail do usuário: ")
        deletaNome(procurado)


    #opção 5
    if opcao == 5:
        print("Editar usuário por email:")
        print("-----------------------------")
        alteraUsuario()
