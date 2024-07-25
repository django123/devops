pipeline{
    agent any

    parameters {
            string(name: 'PERSONNE', defaultValue: 'M. JENKINS', description: 'A qui devrais - je dire bonjour?')
            text(name: 'BIOGRAPHIE', defaultValue: '', description: 'Entrez les informations sur la personne')
            booleanParam(name: 'TOGGLE',defaultValue: true, description: 'Activez cette valeur')
            choice(name: 'CHOIX',defaultValue: ['UN', 'DEUX', 'TROIS'], description: 'Faites un choix')
            password(name: 'MOT_DE_PASSE',defaultValue: 'SECRET', description: 'Entrez un mot de passe')
    }

    stages{
         stage('Example'){
                options {
                    timeout(time: 1, unit: 'HOURS')
                }
                steps {
                    echo "Hello World!"
                }
        }

        stage('Example 2'){
            steps{
                echo "Bonjour ${PERSONNE}"
                echo "Biographie ${BIOGRAPHIE}"
                echo "Toggle ${TOGGLE}"
                echo "Choix ${CHOIX}"
                echo "Mode de passe ${MOT_DE_PASSE}"
            }
        }

        stage("A"){
            steps{
                echo "====++++executing A++++===="
            }
            post{
                always{
                    echo "====++++always++++===="
                }
                success{
                    echo "====++++A executed successfully++++===="
                }
                failure{
                    echo "====++++A execution failed++++===="
                }
        
            }
        }
    }

   


}