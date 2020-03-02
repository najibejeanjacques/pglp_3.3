# pglp_3.3

1) Cette solution ne respecte pas le principe LSP, car si on remplace une instance de Robot par RobotStatique on peux avoir une erreur ( On peut avoir un comportement innatendu pour l'utilisateur), ce qui explique que le principe LSP n'est pas respecté.
(Un robotStatique ne bouge pas, c'est pour cela on a lancer une exception avec la methode avance au niveau de robotStatique, ce qui entraine qu'on ne peut pas remplacer une instance de robot par robotStatique sans altérer le comportement).

2) Implémentons la méthode avancerTous qui fait avancer tous les robots:

        class TousLesRobots
        
        
        
        
3) Proposons une solution respectant LSP:

  -Créons d'abord une interface robot
                                                                                                        
        interface Robot
        {
                public function deplaceAutrement(); 
        }
  -Créons la classe robotBase qui contient la méthode avance de base
  
        class RobotBase
        {
                private Direction direction;
                pricate Position position;
                
                public void avance()
                {
                        /*avance d'une case*/
                }
        }
        
   -Créons la classe robotStatique qui ne possede pas la methode avance, mais une autre methode avec un traitement different
   
        class RobotStatique implements Robot 
        {
                private $robotBase;
                public RobotStatique(RobotBase $robotBase)
                {
                        this.robotBase = $robotBase;
                }
                
                public function deplaceAutrement()
                {
                        //traitement pour un robot statique
                }
        }
