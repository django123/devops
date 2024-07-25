pipeline{
    agent any

    environment{
        MY_VAR = 'une variable'
        MY_NUMBER = 123
    }

    stages {
       
            stage('Example'){
                options {
                    timeout(time: 1, unit: 'HOURS')
                }
                steps {
                    echo "Hello World!"
                }
            }
        }
        
        
    }
}