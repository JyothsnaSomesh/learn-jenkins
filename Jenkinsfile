pipeline {
    agent {
    node {
        label 'Agent-1'
        }
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
                echo 'Deploying'
            }
        }
    }
//Post Build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}


    