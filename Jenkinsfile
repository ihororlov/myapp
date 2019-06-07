pipeline {
    agent { 
        label 'node1'
        }
    stages {
        stage('Example') {
            agent {
                dockerfile true
            }
            steps { 
                sh 'pwd'
                echo 'Hello World'
                sleep 5
            }
        }
    }
}
