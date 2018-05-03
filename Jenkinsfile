pipeline {
    withEnv(['docker=/usr/local/bin/docker']) {
        sh 'docker --version'
    }
    agent {
        docker {
            image 'maven:3.5.3-alpine' 
            args '-v /root/.m2:/root/.m2'
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
