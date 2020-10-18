pipeline {
    agent {
        docker {
            image 'buid_docker_image:latest'
            args "-v /var/run/docker.sock:/var/run/docker.sock"
        }
    }
    stages {
        stage('Copy source code') {
            steps {
                git 'https://github.com/savik1/boxfuse-sample-java.git'
            }
        }
        stage('Build war') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Make docker image') {
            steps {
                git 'https://github.com/savik1/docker-tomcat.git'
                sh 'docker build -t myweb .'
                // docker tag
                // docker login
                // docker push
            }
        }
    }
}
