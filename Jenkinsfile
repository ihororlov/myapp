pipeline {
    agent { 
        label 'node1'
        }
    stages {
        stage('Remove Container') {
            steps {
                sh 'sudo docker rm -f c1 || /bin/true'
            }
        }
        stage('Build Image') {
            steps {
                sh 'sudo docker build -t gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2 .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'sudo docker run --name c1 -d -p 80:80 gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2'
            }
        }
   }
}
