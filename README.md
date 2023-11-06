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
	
_______________________________________________________________________________

2.04 EXEMPLOS DE FUNÇÕES
_______________________________________________________________________________


	CONSTANTE
	F(X) = C ---> NÃO DEPENDE DO VALOR DO DOMINIO(CONSTANTE)
	V(T) = 20
	UMA RETA NA VERTICAL
	
	LINEAR
	F(X) = ax + b
	F(D) = 5 + 2D
	UMA RETA ENTRE X E Y, UMA RETA VERTICAL 
	
	FUNÇÃO QUADRATICA
	F(X) = ax² + bx + c
	H(T) = S - ST²
	GRAVIDADE, CURVA 	

	F(X) = x³ + 10x² +5x
	COMPARAÇÃO AO UMA MONTANHA RUSSA

	FUNÇÕES RACIONAIS
	F(X)= (P(X))/Q(X); F(X)= 1/X
	RAZOES DE POLINOMIO
	POTÊNCIAL DE LEONAR JONES
	U(raio) = A/R¹² - B/R³+³
	ENERGIA DE LIGAÇÃO
	
	FUÇÕES TRIGONOMÉTRICAS
	F(X) = SEN(X)
	F(X) = COS(X)
	F(X) = TG(X) = (SEN(X))/COS(X)
	Série de Fourier
	SÃO ONDAS, LEMBRO COMO LAMBIDA 
	
	FUNÇÕES EXPONÊCIAIS
	F(X) = CONSTANTE.e^bx
	N(T) = N0.E^rt (calculo do virus)
	QUANDO SEMPRE CRESCE E TEM UM GRANDE CRESCIMENTO DE UMA HORA PARA OUTRA
	
	FUNÇÃO DE SIGMÓDE (CIENCIA DE DADOS, GRANDE IMPORTÂNCIA EM PROGRAMAÇÃO)
	REDES NEORAIS
	LETRA GREGA SIGMA= VOU COLOCAR COMO &
	&(X) = 1/(1+e^-x)
	ELA NUNCA É MENOR QUE 0 OU MAIOR QUE 1
	
_______________________________________________________________________________

2.05.6 CONCEITOS DE LIMITES
_______________________________________________________________________________


	LIMITES:
	
	F(X)= 1/X
	QUANTO MAIS PROXIMO DE 0 O X FOR, MAIS ALTO O VALOR RESULTANTE 
	LIM F(X) = 0 TENDE-SE AO INFINITO
		
	LIMITE LATERAIS
	F(X)= 1/X , Xe|R
	LIM ---> 0
	SEMPRE CAMINHANDO A PERTO DE 0 DO X POSITIVO PARA INFINITO POSITIVO
	SEMPRE CAMINHANDO A PERTO DE 0 DO X NEGATIVO PARA INFINITO NEGATIVO
	SEMPRE DEPENDENDO DO LADO POSITIVO OU NEGATIVO
	+X POSITIVO = +INFINITO = 0
	-X NEGATIVO = -INFINITO = 0
	F: |R =! {0} --->|R 
	X ---> F(X)=1/X
	
	LIM F(X) = ?
	X = +INFINITO E X = -INFINITO
	
	LIM (X+1)/2X+1
	X = INFINITO
	
	LIM 1/X = 0
	X = INFINITO
	LIM 1/X = 0
	X = -INFINITO
	
	LIM (X+1)/2X+1 = X(1+((1)/X))/X(2+1) = (1 + (1/X))/(2 + (1/X)
	LIM 1/X = 0
	X = 1/2 == LIM F(X) == -INFINITO == +INFINITO
	
	*GRAFICO = É UMA ASSINTOTA VERTICAL*

_______________________________________________________________________________

2.07 DERIVADAS - INTUIÇÃO E NECESSIDADE
_______________________________________________________________________________


	DISTÂNCIA DE DOIS PONTOS
	D= DISTANCIA
	D = 435 KM
	T = TEMPO
	T = 6 HORAS
	V = VELOCIDADE MEDIA
	V = D/T
	V 435/6 = 72,5 KM/H
	
	VELOCIDADE COMO UMA FUNÇÃO DO TEMPO
	V(T)
	
	*COMO DEFINI VELOCIDADE INSTANTÂNIA*
		-----------------------------
		|v = VELOCIDADE INSTANTÂNIA |
		|	v =  ΔX/ΔT              |
		|	v(T) = LIM ΔX/ΔT        |
		|	ΔT = 0                  |
		-----------------------------
	
	ΔT ----> DT QUANDO O LIMITE DE ΔT VIRA 0, CHAMAMOS DE 'DT'
	ΔX ----> DX
	--------------------
	|v(T) = (DX(T))/DT |
	--------------------
	
	DERIVADA É UMA FORMA DE MEDIR AS VARIAÇÕES
	DERIVADA <=> VARIAÇÕES {(DE)CRESCIMENTO}
	
	FUNÇÃO CONSTANTE
	F(X) = C
	
	DF/DX = 0
	
	FUNÇÃO LINEAR
	F(X) = AX+B
	
	DF/DX > 0
	
	FUNÇÃO QUADRATICA
	F(X) = AX² +BX +C
	
	DF/DX < 0 NEGATIVA 
	-----------------------------------------
	|EXISTE UM UNICO PONTO QUE A FUNÇÃO FICA| 
	|DF/DX = 0  O VALOR MINIMO DA FUNÇÃO    |								
	-----------------------------------------
	DF/DX < 0 POSITIVA 
	
_______________________________________________________________________________

2.08 DERIVADAS - CONSTRUÇÃO GEOMÉTRICA
_______________________________________________________________________________


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

	DF/DX = LIM ΔF/ΔX
	ΔX ---> 0
	X = {1,2,3}
	ΔX = 2 - 1 = 1
	ΔF = 4 - 1 = 3
	ΔF/ΔX = 3/1 = 3
	
		   /| 	
		  / |
	TG	 / _| ΔF
		/_|_| 90º
		ΔX
	ΔX ---> 0 
	DX PARA VIRAR UMA TANGENTE PARA FORMA UMA RETA NA TANGENTE
	ESTÁ RELACIONADO A INCLINAÇÃO DA RETA TANGENTE A O PONTO X
	
	TG∅ = ΔF/ΔX
	LIM DX ---> 0 APROXIMA
	TG∅ = DF/DX 
	
	EXISTE UM MOMENTO QUE O PONTO FICA RETO
	NO MOMENTO:
	DF/DX = 0 
	CRITEIRO PARA ENCONTRAR O PONTO MINIMO E MAXIMO
	MAIOR PONTO É CONSIDERADO O MAXIMO GLOBAL 
	O OUTROS PONTOS MAIORES SÃO CHAMADOS DE MAXIMO LOCAL 
	MENOR PONTO É CONSIDERADO O MINIMO GLOBAL 
	O OUTROS PONTOS MENORES SÃO CHAMADOS DE MINIMO LOCAL 
	
	RELACIONADO A ÀREA DE OTIMIZAÇÃ,
	DF/DX = 0 == PONTO DE ÓTIMO
	
	DERIVADOS DE SEGUNDA ORDEM
	D²F/DX² = (D/DX/).(DF/DX)
	CONCAV CIMA
	D²F/DX² > 0
	CONCAV BAIXO
	D²F/DX² < 0
	
	
-------------------------------------------------------------
-------------------------------------------------------------