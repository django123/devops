pipeline{
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages{
        

        stage('Build'){
            steps{
                echo "Etape 2 de construction en cours"
            }
        }
        stage('Test'){
            steps{
                echo "Etape  de test en cours"
            }
        }
         stage('Deployment parallèle'){

            failure true
            parallel {
                stage('Deployement Dev'){
                    steps {
                        echo "Etape de deployment dev en cours"
                    }
                }

                stage('Deploiment en stagin'){
                    steps {
                        echo "déploiement en stagin"
                    }
                }
            }
           
            steps{
                echo "Etape  de depoiement en cours"
            }
        }
       
    }

   


}