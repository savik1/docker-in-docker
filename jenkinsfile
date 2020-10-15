pipeline {
    agent {
        docker {
            image 'buid_alpine_maven:latest'
        }
    }
    stages {
        stage('Copy source code') {
            steps {
                git 'https://github.com/savik1/boxfuse-sample-java.git'
            }
        }
        stage('Build jar') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Make docker image') {
            steps {
                git 'https://github.com/savik1/docker-tomcat.git'
                // docker build
                // docker tag
                // docker login
                // docker push
            }
        }
    }
}
