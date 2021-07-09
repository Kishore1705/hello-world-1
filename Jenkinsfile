pipeline {
  agent { label 'javamaven' } 
    stages {
        stage('Directory') {
            steps {
                sh 'cd /home/slave5/workspace/javapipelinejob/hello-world-1/'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp /home/slave5/workspace/javapipelinejob/hello-world-1/target/hello-world.war /opt/tomcat/webapps'
            }
        }
       stage('Run') {
            steps {
                sh '/opt/tomcat/bin/./startup.sh'
            }
        }
    }
}
