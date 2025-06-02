Primeiras ideias:
bot automatizar coisas simples (mudar embed)
salvar personagens (criar interface)
pegar dados dos players a cada certo tempo
criar sistema de tokens pra salvar personagens
bot dar premiações automaticamente
criar canal só para o bot
criar interface de save
espécie de termo com recompensa aleatório
inventário com medalhas de buffs permanentes 

1° interface e dados:

	Cadastro de usuários por meio de comando. Comando vai dar cargo para liberar para jogar e coletar dados.
Dados coletados: apelido, id do usuário e vai comunicar com o banco de dados. Vai impossibilitar o comando start.
	Banco de dados: apelido, id, xp, lvl.
	banco de dados(outro) com dados relacionados ao mudae, harém, kakera, etc.
	comando profile buscou template, buscar dados do usuário, buscar dados do mudae, criar mensagem, enviar pro usuário uma embed.
	calcular médias de dados (kakera e outros números)
	coleta de dados do banco de dados, organizar dados e criar mensagem (embed)

2° sistema de lvl (lvl 1000 max):

	Sistema(ganho de xp): ler cada mensagem enviada em info-mudae e roleta, ler id, identificar usuário no banco de dados, vai editar o xp do usuário, 2 xp por mensagem.
	sistema de nível pós max lvl 1000 com metas de xp e não nível ou lvl ilimitado (ambos com recompensas reduzidas).
	definir base de xp e escalonamento

3° automatizar tudo (premiações)

	pegar nome do personagem de dentro de um banco de dados, checar se esse personagem aparece na roleta, se aparecer ler nome do usuário, pegar id, premiar.
	base: ler dados do usuário (apelido/id), pegar lógica de cada tipo de premiação, checar se cumpri os requisitos e premiar.
	se a pessoa possui 0 de kakera e possui lvl x a pessoa ganha um valor de kakera pra deixar mais equivalente à média de kakera dos players do server.

4° sistema token com base no lvl

	player.token (dentro de player vai ter token). token no profile. a cada x lvls ganha x tokens.
	comando(save): vai verificar se o usuário possui token, se ele n tiver manda mensagem avisando que n possui condições de usar, se tiver manda mensagem de confirmação, se sim, mandar mensagem pra player digitar qual personagem quer salvar, ver se o personagem está na coleção do usuário, se tiver, salva, se não digite novamente ou exit.
	function: pega o nome do personagem e linka com o id do usuário que salvou ele.
	pode adicionar uma nota ao personagem pra deixar isso visivel.
	personagens ficarem salvos no banco de dados para serem devolvidos na temporada seguinte.

5° algum minigame de kakera diário

	comando(minigame): uma vez por dia, kakera base 1000, kakera max(com buffs) 10000, se ganhar ele consegue kakera, se não deixa de ganhar.
	definir minigame
	verificar se usuário já usou o comando dentro de 24h.

6° inventário com medalhas de buffs permanentes (página de profile ou interface)
	
	outra interface/página. outros dados sendo salvos no banco de dados (talvez criar um separado só pro inv).
	as medalhas são definadas por temas de temporada sendo limitadas, sendo dadas por eventos e missões que requerem certo lvl.
	são objetos, guardam atributos.
	cada medalha precisa de um lvl específico mais missões.
	buff ganho de kakera no minigame em x%; ganho de kakera da arena; ganho de kakera objetivo da temporada; e mecânicas futuras.
