pipeline{
    agent any
    stages{

         stage('Example'){
                options {
                    timeout(time: 1, unit: 'HOURS')
                }
                steps {
                    echo "Hello World!"
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