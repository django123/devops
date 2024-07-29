pipeline{
    agent any


    stages {
        

        stage('Build et Test '){
            steps{
                echo "Construire et tester l'application"
            }
        }
        stage('Deployment parallèle'){

            failFast true
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

        }
       
    }

   


}