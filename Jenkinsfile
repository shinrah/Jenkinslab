pipeline {
    agent any 
    
    parameters {
  choice choices: ['dev ', 'test', 'prod'], description: 'select the environment ', name: 'environment'
  choice choices: ['main', 'shinrah'], description: 'select the branch', name: 'gitbranches'
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
                
         stage ('Build') {
            steps {
                echo 'Building the java applicaiton'
                sh 'mvn clean package'
            }
        }
    }
}
