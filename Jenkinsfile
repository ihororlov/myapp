pipeline {
    agent { 
        label 'node1'
        }
    stages {
        stage('Remove Container') {
            steps {
                sh 'docker rm -f c1 || /bin/true'
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker build -t gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2 .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run --name c1 -d -p 80:80 gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2'
            }
        }
   }
}
