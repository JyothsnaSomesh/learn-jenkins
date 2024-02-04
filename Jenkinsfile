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
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
            }
            steps {
                sh """
                    echo "I wrote shell-script'
                    env
                """
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


    