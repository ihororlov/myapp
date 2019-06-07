pipeline {
    agent { 
        label 'node1'
        dockerfile true
        }
    stages {
        stage('Example') {
            steps { 
                echo 'Hello World'
                sleep 5
            }
        }
    }
}
