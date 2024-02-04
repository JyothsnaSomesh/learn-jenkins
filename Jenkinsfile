pipeline {
    agent {
    node {
        label 'Agent-1'
        }
}
environment { 
        GREETING = 'Hello Jenkins'
    }
//Build
    stages {
        stage('build') {
            steps {
                echo 'Building..'
            }
            
        }
        stage('test') {
            steps {
                 echo 'Testing..'
            }
           
        }
        stage('deploy') {
            steps {
                sh """
                    echo "I wrote shell-script'
                    env
                """

            }
                
            }
        }
    }
//Post Build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'say its a failure'
        }
        success { 
            echo 'It is a Success'
        }
    }
}


    