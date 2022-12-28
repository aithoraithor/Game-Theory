# Game-Theory
Game Theory

	Game theory is the study of strategic decision making. It is often used in economics, political science, and psychology as a tool that can be used to model and analyze strategic interactions between different agents.	 	It focuses on formulating a model of decision-making by identifying the players’ goals, and possible strategies. It is a way of thinking about strategic situations in which people are trying to achieve their goals while taking into account the goals of others. Game theory suggests that the outcome of a game is influenced by the actions and decisions of all the players involved in the game, and it is based on the concept that the payoff from one player is dependent upon the strategies or the decisions of the other player/players.

Some terms and concepts:

Game: It is a situation in which two or more players interact with each other to attain certain goals. It includes the modeling of conflict among nations, political campaigns, companies, and trading behavior in markets.

Strategy: It is a plan of action taken by players in order to achieve their goal and to deal with the various circumstances that may arise in the game.

Players/Agents: Are the participants in the game. Players normally make decisions to maximize their payoff (gains). 

Control theory: is a branch of mathematics that deals with the control of systems, is the study of how a system's inputs influence its outputs. It is used to design systems that can achieve desired objectives while avoiding undesired states. In control theory, a hypothesis is first proposed and then tested through simulation.

Nash equilibrium: It is a state of balance in which each player has no incentive to change their current course of action. It is a situation where no player can pick an alternative strategy and be better off if the other players maintain their strategy.

GrimTrigger: It is a game theory strategy in which players cooperate with each other as long as both players are behaving cooperatively. However, if one player deviates from the cooperative behavior, the other player will also deviate (or "trigger"), leading to a situation where both players are worse off.

Maloch: It is a term used in sociology to refer to someone who demonstrates a hostile or aggressive attitude towards others. It may also be described as the god of perverse game theory. 

Backward induction: It is a process of reasoning backwards in time, from the end of a problem or decision process, to determine what action should be taken at each previous step.

Multi-polar trap: It is a game theory scenario in which two or more players are each trying to achieve the same goal, but their actions end up preventing any of them from achieving it.

Types of games:

Below you can find some of the main types of games possible:

Cooperative vs. non-cooperative games: In cooperative games, players have an incentive to work together in order to achieve the best possible outcome for all players. In non-cooperative games, players do not have this incentive and may instead act in their own best interest.
	Normally the cooperative game is based on a mandatory binding contract that can be reached by all parties on the basis of information exchange, mutual trust, and commitment through negotiation and communication. In a cooperative game, players have to compete in groups ("coalitions") due to the possibility of external enforcement of cooperative behavior (e.g., through contract law). 	Often, the key difference between cooperative games and non-cooperative is the absence of external authority to establish rules enforcing cooperative behavior. In the absence of external authority (such as contract law), players cannot forge alliances and must compete independently, or all agreements need to be self-enforcing (e.g., through threats).

Symmetric vs. asymmetric games: A symmetric game is a game in which the players have the same roles and the same information about the game state. An asymmetric game is a game in which the players have different roles and/or different information about the game state.

Zero-sum vs. non-zero-sum games: A zero-sum game is a game in which the total payoff for all players is equal to zero; they are also considered non-cooperative games. A non-zero-sum game is a game in which the total payoff for all players is not equal to zero.

Simultaneous vs. sequential games: In simultaneous games, all players make their decisions at the same time, meaning they choose their strategy without knowing the strategy of the other players. In sequential games, players make their decisions one after the other, and each player has full information about the previous moves of the other players.

Perfect information vs. imperfect information (bayesian games): Information set is the pieces of information that are given at any specific time during the game. In perfect information games, all players have complete information about the game state. In imperfect information games, some players may have incomplete information about the game state.

The prisoner's dilemma: It is a game theory scenario in which two prisoners must decide whether to cooperate or defect. If they both cooperate, they each receive a small reward. If they both defect, they each receive a small punishment. However, if one defects while the other cooperates, the defector receives a large reward while the cooperator receives a large punishment.

Types of strategies:

	There are many different strategies that can be used in game theory, and the best strategy in any given situation will depend on the specific rules of the game, the motivations of the players, and the expected outcomes of different actions. Here are a few examples of common game theory strategies:
Tit for tat: As mentioned in a previous answer, tit for tat is a strategy that involves reciprocating the actions of an opponent. A player using this strategy will cooperate with their opponent on the first move, and then will mimic the opponent's previous move on subsequent rounds.

Always cooperate: This strategy involves always choosing to cooperate, regardless of the actions of the opponent. This strategy is often used when the players have a long-term relationship and there is an incentive to build a reputation for cooperation.
Always defect: This strategy involves always choosing to defect, regardless of the actions of the opponent. This strategy is often used when the players do not have a long-term relationship and there is no incentive to cooperate.

Conditional cooperation: This strategy involves cooperating with the opponent if and only if the opponent has cooperated in the past. This strategy is similar to tit for tat, but it does not require the player to cooperate on the first move.

Mixed strategy: This strategy involves randomly selecting between different actions with certain probabilities. For example, a player might choose to cooperate with probability p and defect with probability (1-p). This strategy can be used to confuse the opponent and make it difficult for them to predict the player's actions.

Control theory and agent-based model

	Control theory is a branch of mathematics that deals with the control of systems— it is the study of how a system's inputs influence its outputs. It is used to design systems that can achieve desired objectives while avoiding undesired states. In control theory, a hypothesis is first proposed and then tested through simulation. 
	An agent-based model (ABM) is a computational tool for simulating the actions and interactions of autonomous agents (such as individuals or organizations) to understand the behavior and outcomes of a system. It combines elements of game theory, complex systems, emergence, computational sociology, multi-agent systems, and evolutionary programming.

Tool used to simulate: agent model modulation in Netlogo.

Setting the game:

Introduction  
	Processes of cooperation and conflict are always the subject of study for game theory. As previously mentioned, the prisoners dilemma is probably one of the most famous and interesting cases. It is a very simple game (in essence) with two players and two strategies. Each player has a dominant strategy, which gives him a better payoff for all situations. But when players play dominant strategies, they get worse payoffs compared to a situation when they do not. So rationality demands agents to choose dominant strategies (it is the only Nash equilibrium in this game), but general efficiency call for cooperation. The dilemma arises because each prisoner has an incentive to defect, even though they would both be better off if they cooperated. If one prisoner knows that the other is going to cooperate, then it makes sense for them to defect in order to receive the large reward. However, if both prisoners defect, then they both receive the small punishment. 	During experiments, humans cooperate in about 40% of cases demonstrating different behavior - they create long chains of cooperation and sometimes defect. This is a striking contrast with theory and brings new ideas about this game. Researchers tried to consider iterative setup, but any finite step game leads to the same theoretical result - always defect. This is because we can solve the game from the end using backward induction - in the last round, the best option is for both players to defect, so on the pre-last round and so on.
	The solution was found in an indefinite ending. When players play the game iteratively, the probability of finishing the current round is equal to some delta. In this case, there is a cooperative equilibrium solution under the threat of retaliation. If players use strategies GrimTrigger (or unforgiving in Netlogo) each player cooperates with the other until it defects. After that, one specific player defects against this player forever. In this simulation model, we will try to understand how different strategies evolve in interactions between countries. 

Model 

	To model interactions between countries, we create several agents, connected by links. The general idea is the following:

Each country has key attributes: strategy and wealth.
Each country can be linked to other countries (the number of links varies and can be 0).
In each step, each country tries to partner with another linked country. If this happens, they become partners for this round.
Partnered countries play the prisoners' dilemma game, which can be considered to realize some agreement. If both countries cooperate - they both get a reasonable payoff (which is added to their wealth). If one country cooperates and another defect - defecting country gets all payoff, and the other country gets 0. If both countries defect - they both get a small payoff. So each country has an incentive to defect.
	
	In this model, we implement three additional features (controlled by interface), crucial for model dynamic understanding, which can create a rich model with unusual behavior:

Each country can change its own strategy to a strategy that gives the best payoff for neighbors (linked countries) or all countries. 
Each country can cut the link to defecting country (with some probability). 
Each country can establish a new link with another country with some predefined probability. 

Netlogo implementation 
 
	Agents are countries that can play a game with linked countries (one game per round). They can also estimate their strategy effectiveness and change, if possible, to the best strategy of neighboring countries (or all countries).
	Besides, there is a possibility to cut connections with countries that defect from a country and establish new links with other countries. 

Attributes 

Each agent has attributes  countries-own [  	wealth ; wealth amount
	strategy ; current strategy
	defect-now? 	partner-defected? ;;action of the partner 	partnered? ;;am I partnered? 	partner ;;WHO of my partner (nobody if not partnered)  	partner-history ;;a list containing information about past interactions 
		;;with other countries (indexed by WHO values) 
] 

Initial state 

	Initially, countries are generated as a random graph. Make sure you press layout, so Netlogo creates proper visualization.

Sliders define a number of initial strategies.
Button make-full-graph is to be pressed when no other links are created (so before pressing, put num-links to 0 and set up countries). 

Interface 

The typical interface is on the following image:

 
Set up is on the left side: 
The middle is simulations control
Simulate-1-round simulates one round.
Simulate-n-rounds do n-rounds simulation, where n-rounds is defined by the slider. Switches can be changed between rounds; they are naturally named.
The right side contains monitor and two plots.
Each plot can be exported by right-clicking to csv or as an image. 




Simulations can be performed using tools->behavior space. And you can perform them either through the web version or by downloading the application. For more information, check the website: https://ccl.northwestern.edu/netlogo/

The code is saved in the Github repository: missing the link

Experiments 

	1) Static setup (static strategy and link control)

	If we begin with non-zero games and if there are enough cooperators (which are the main source of wealth for defectors) then defectors get a huge lead initially. But after they defect enough tit-for-tat players, especially unforgiving ones, their payoff starts to decrease. In the concrete case, it strongly depends on the connectivity of the graph. Sometimes defectors keep their lead. In international relations, this is a situation when you can't do much about the situation and must work with every country, even perverse ones.

	2) Dynamic strategy and static links

	Consider the initial state with 80 cooperative agents and three defecting. To start, we allow agents to change strategy but don’t allow them to change links. Here we have a typical dynamic, where all agents evolve to defecting because defecting gives a better payoff. This is the world of Maloch - perverse game theory. 
	In this scenario the result depends on the initial number of strategy types. For fast exploration, there are three possible outcomes. 1) Defectors win over and everyone defects everyone. This often represents the world of real politics. 2) Defectors and random players are winners. They divide the world in some dynamic equilibrium. This world is less predictable than the previous one. 3) Retaliators, those who are adepts of "eye for eye" principle (players cooperate if and only if both receive the same payoff) are the winners. They cooperate with each other and are ready to punish everyone who tries to defect them.
		


	3) Static strategy and dynamic links

	Suppose we are in a static world, where countries can't change their behavior strategy but can at least cut links to bad countries and sometimes try to establish new links with others. Here we allow the player to create new ties. Now we have one single cooperative cluster. All defectors naturally fade away. But initially, they have a huge profit. Nevertheless, they lose too many cooperators. 	
	When we allow for cutting links but keeping the same strategy we see an interesting change - no one wants to be connected with red defectors. Their number is stable because agents here change their strategy based on neighbors' payoffs, so if they do not have neighbors - there is no change. 	
		


	The typical picture is that we have a strong central cluster of cooperators countries. And periphery is filled with defectors and random movers who defect half of the time. This can represent the current status of the war between Russia and Ukraine - right now, we have cooperators inside West and periphery with defectors and "weak states", unable to keep one policy. Sometimes center countries try to establish a new link with periphery states (in the hope they change and can provide long-term cooperation). But without strategy changes result is the same. Interesting, that means the wealth of retaliators here is the highest, defectors are next, and cooperators are the losers (with random ones).



	


	
	4) Dynamic strategy and links

	Another interesting setup is, to begin with, an equal number of different strategies to see what strategy will win. Right now, it seems that any collaborative (not defect) strategy has a chance. But it needs additional computations to investigate. 
	If we have a full graph (with all possible links), defectors will win in any situation. Even if there is only one defector initially. So connectivity is crucial for defector spreading. For a less connected graph, if any retaliator (tit-for-tat and unforgiving) strategy is present - they will win at the ending. 
	However, the result actually depends on the initial condition. If you have enough cooperative players - they have a chance to win. An interesting dynamic of victory - a first huge cluster of cooperators cut off defectors and then work inside to make wealth, step by step moving defectors to their side (because they change strategy for most successful among neighbors). The best outcome is a non-obvious idea - cut, make wealth, connect and show superiority of cooperation.



	
Conclusion:

	As suggested by Robert Axelrod, the experiments confirm that tit for tat shows to be a great strategy for cooperation. It is an effective way to deter aggression while still cooperating. An agent using this strategy will first cooperate, then subsequently replicate an opponent's previous action, either cooperate or defect. Since its introduction, it has been used in natural sciences and social sciences as a way to explain evolution and conflict resolution. 
	Another big takeaway from this and many other game theoretic games is the need for repeat interactions, win-win dynamics (non-zero-sum), and communication to enable opportunities for cooperation to emerge. They are essential as they facilitate players to learn about each other's preferences and intentions, develop trust, and achieve benefits for both parties involved.  	We are nature and nurture. In the same way, the game defines the player, in the long run, the players define the game. We are bounded to find ways to cooperate with each other if we want to safeguard the future of humanity. As players, we need to do our best to evolve cooperation through time, so we can maybe one day become whole.
