# pglp_3.3

1) Cette solution ne respecte pas le principe LSP, car si on remplace une instance de Robot par RobotStatique on peux avoir une erreur ( On peut avoir un comportement innatendu pour l'utilisateur), ce qui explique que le principe LSP n'est pas respecté.

2) Implémentons la méthode avancerTous qui fait avancer tous les robots:

        class TousLesRobots
