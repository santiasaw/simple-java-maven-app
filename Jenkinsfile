pipeline {
	agent {
        docker {
            image 'maven:3.9.0'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('cloneRepo') { 
            steps {
                git 'https://github.com/santiasaw/simple-java-maven-app'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            } 
        }
    }
}