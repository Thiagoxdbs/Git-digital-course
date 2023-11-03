_______________________________________________________________________________

01 - Git/Versionamento
_______________________________________________________________________________

Versionamento:

	Utilizado em projeto para fazer versoes
	determinar o ponto que está no software 
	registo em arquivos de codigo, mas não precisa ser nescessariamente me codigo
	podendo voltar ou comentar um codigo em uma certa parte 
--------------------------------------------------------------
O que é git:

	git é um sistema de versionamento de codigo, que guarda os registros de versão como snapshots, com referencias

	rest = registro do codigo 

	O git é muito rapido por ser feito operações locais, enquanto ainda desenvolve

--------------------------------------------------------------
GIT COMANDOS

			Git --version vê a version
			git clone "url" cria uma versao da pasta do github dentro do seu disco 
			exteção git lens
				
			CONFIGURAÇÃO USER
				git config --global user.name ou user.email ""

			INIT 
				git init (arquivo novo)  iniciou um repositorio git

			STATUS
				git status vê como está o andamento dentro da pasta em relação ao git

			ADD arquivos ao stage
				git add "file" adiciona o arquivo em expecifico 
				git add . adiciona todos
			
			Restauração
				git restore --staged 'file' volta para o estado anterior
			
			DIFF MODIFICAÇÕES
				git diff mostra as linhas modificadas 
				git diff --staged 
			
			COMMIT
				git log traz todos os ultimos commits
			
			Arquivos PULL	
				git fetch vê os arquivos que vão ser baixados pelo git
				git diff origin/main mostra os arquivos que vão entrar pelo git pull
			
			branch
				git branch nome_branch cria uma branch
				git log --online --decorate indica aonde está o head
				git checkout -b nome_branch muda a branch
				git branch mostra todas as branchs
				git merge nome_branch traz o conteudo da branch solicitada
				
--------------------------------------------------------------

	untracked = passa direto para o staged
	add the file

	unmodifiel = arquivo já está mapeado pelo git, passou para um processo de staged e commit
	remove the file
	edit the file

	modifiel = o arquivo foi modificado na podendo
	stage the file

	staged = estado antes do commit
	commit 
 
-------------------------------------------------------------
obs:

'Pasta .gitignore ignora arquivos no git'

_______________________________________________________________________________

2.02 - Cálculo Básico
_______________________________________________________________________________


Funções - Definições

--Relação 

	Conjuntos A, B;
	Pronduto Cartesiano AxB = {(A,B), a&B; b$B}
	A = {1,2,3}
	B = {4,6}
	AxB = {(1,4),(1,6), (2,4), (2,6), (3,4), (3,6)}

		B
		6| .-.-.
		4| .-.-.
		 |
		 |_._._.__> A
		   1 2 3
		
	Relação: Rc AxB# ------> R{(2,4),(3,6)}
	
	R será uma função: V(ParaTodos)aeA & B:(a,b)eR
	---------------
	| F: A ---> B |
	|    a ---> b |
	|    F(a) = b |
	---------------
	
		A domínio de F
		B contradomínio de F
		
		Im(F) = {beB: &aeB com F(a) = b}
	
-------------------------------------------------------------
	
		A = {1,2,3,4}
		B = {0,2,4,6,8,10}
	
	Diagrama de Venn
	
	F:	(A,B)
		(1,2)
		(2,4)
		(3,6)
		(4,8)
	
	Im(F)c B
	Im(F) = {2,4,6,8}
	
-------------------------------------------------------------
	Injetoras:
	Sempre que todos os elementos da imagem recebem do domínio
	
	Exemplo:
		A = {1,2,3}
		B = {2,4,6}
		F:
			(1,2)
			(2,4)
			(3,6)

-------------------------------------------------------------
	Sobrejetoras:
	Elementos da imagem com o mesmo valor podem receber mais de uma variavel A
	Funções sobrejetoras possuem todos os elementos do contradomínio.
	A imagem de uma função sobrejetoras é igual ao seu contradomínio.
	
	Exemplo: 
		A = {-2,2}
		B = {4}
		F: 
			(-2,4)
			( 2,4)
	OBS: X = X² 
	NÃO PODE TER FUNÇÃO DO DOMINIO NO CONTRADOMINIO
	
-------------------------------------------------------------
	Bijetoras:
	Para uma função ser bijetora, não é possível que dois elementos diferentes do 
	domínio sejam associados a um mesmo elemento na imagem. Assim, a principal propriedade 
	de uma função bijetora é que todos os elementos do domínio sejam associados a elementos diferentes 
	na imagem.	
-------------------------------------------------------------
	Expressão funcional, gráficos e paridade
	
	F: |R ---> |R
		X ---> F(X)
		
	Expressão funcional = Funções
	Exemplo:
		F(X) = 2X + 1
	
	Grafico feito em plano cartesiano para colocação do conjunto X e Y.
		
		X = {1,2,3}
		F(X) = 2X
		
		Y
		6|     .
		4|   .
		2| .
		 |_______> X
		   1 2 3
	
	
		F(X) = X²
	
				Y
			.	|	.
			.	|	.
			.	|	.
			_______.|.__________> X
				|  
				|
				|
				|

			
		F(X) = X³
			
				Y
				|	.
				|	.
				|	.
			_______.|._______> X
				|  
			.	|
			.	|
			.	|

	
	Paridade:
	
		F(-x) = F(x)  : Par		= F(x) = x²
		F(-x) = -F(x) : Ímpar 	= F(x) = x³ 		
  
_______________________________________________________________________________

2.03 - FUNÇÃO INVERSA E COMPOSIÇÃO
_______________________________________________________________________________

FUNÇÃO INVERSA:


	F(X)	F:|R --->|R
			   X --->F(X)
			   
	F-¹(X) 
	CONTRADOMINIO ---->DOMÍNIO (INVERSO F(X))
	*NEM TODA F TEM INVERSO(NÃO INVESIVEIS)*
	*F É INVERTÍVEL SE F FOR BIJETORAS*
	*Função identidade, conhecida com ID, x = y, sendo F(X)= Y*
	*Função inversa é uma função reflexida com o centro cendo o ID*
	*Exemplo:*
	*F(X)=2X+1 , F-¹ = ?
	*Y = 2X +1 ---> X = 2Y +1 ---> X-1 = 2Y ---> Y = (X-1)/2*
	
	
-------------------------------------------------------------

COMPOSIÇÃO DE FUNÇÕES:

	F:  A ---> B
	G:  B ---> C
	
	*GoF = G(F(X))*
	
	F(X) = 2X +1 
	G(X) = X²
	GoF  = G(F(X)) = (F(X))² = 	(2X +1)² = 4X² +4X +10
	GoF = 4x² +4x +1
	
	FoG = F(G(X)) = 2G(X) +1
	FoG = 2x² +1
	
	
	F-¹(F(X)) = (F(X)-1)/2 = (2X)/2 
	F-¹oF = X 	g(x) = X	
	
-------------------------------------------------------------


-------------------------------------------------------------


-------------------------------------------------------------


-------------------------------------------------------------
