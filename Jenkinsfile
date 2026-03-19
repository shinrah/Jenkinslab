pipeline {
    agent any 
    
    parameters {
  choice choices: ['dev ', 'test', 'prod'], description: 'select the environment ', name: 'environment'
}

    stages {
        stage ('clean up') {
            steps {
                echo 'Cleaning up workspace..'
                cleanWs()
            }
        }
        stage ('check out') {
            steps {
                echo 'checking out code..'
                sh 'git clone https://github.com/shinrah/JAVA-Application-.git'
            }
        }
    }
}
