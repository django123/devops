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
         stage('Deployment production'){
            when {
                allOf {
                    branch 'master'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps{
                echo "Etape  de depoiement en cours"
            }
        }
       
    }

   


}