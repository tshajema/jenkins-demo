pipeline {

    agent {
        label 'maven'
    }

    stages {

        stage('Build') {
            steps {
                echo "Building on ${NODE_NAME}"
                sh 'java -version'
                sh 'mvn -version'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }
}