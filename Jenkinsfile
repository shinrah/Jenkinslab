pipeline {
    agent any 

    parameters {
        choises ()
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
