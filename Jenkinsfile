pipeline {
    agent { 
        dockerfile true
    }

    stages {
        stage('Remove Container') {
            steps {
                docker rm -f c1 || /bin/true
            }
        }
        stage('Build Image') {
            steps {
                docker build -t gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2 .
            }
        }
        stage('Run Container') {
            steps {
                docker run --name c1 -d -p 80:80 gitlab.intecracy.com:4567/devopssoftengi/devops_test/www:v2
            }
        }
   }
}

       