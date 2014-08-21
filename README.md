poolranking
===========
Simple webapp to maintain pool player ranking

Objects
Game(timestamp, players[Player],winner[Player])
Player(name)

Methods
addPlayer(name)
modifyPlayer(Player, newName)
deletePlayer(name)
getPlayers()

addGame(timestamp, players[Player], winner[Player])
deleteGame(Game)
getGames()

//TODO
getRankingList()
	players = getPlayers()
	for(Player : players)
		
	

getPlayerPoints(Player)
	points = 0
	games = getGames()
	for(Game : games)
		if(Player == Game.winner)
			points++
	return points

getPlayerNumberOfGames(Player)
	games = 0
	for(Games : games)
		if(Player in Game.players)
			games++
	return games

getPlayerWinPercentage(Player)
	return getPlayerPoints(Player) / getPlayerNumberOfGames(Player)


