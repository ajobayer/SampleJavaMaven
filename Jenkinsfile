pipeline {
    agent {
        docker {
            image 'maven:3.5.3-alpine' 
            args '-v /root/.m2:/root/.m2:/usr/local/bin/docker'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
