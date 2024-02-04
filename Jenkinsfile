pipeline {
    agent {
        node {
            label 'Agent-1'
        }
    }
    environment { 
        GREETING = 'Hello Jenkins'
    }
    options {
        timeout(time: 1, unit: 'SECONDS') 
    //Build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                 echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "Here is the shell script"
                    echo "$GREETING"
                    sleep 10
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

    