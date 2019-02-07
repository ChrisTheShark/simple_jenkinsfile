pipeline {
    agent none
    stages {
        stage("Build and Test Application") {
            agent {
                docker {
                    label: "docker"
                    image: "openjdk:8u191-jdk-alpine3.8"
                }
            }
            steps {
                sh "java -version"
            }
        }
        stage("Docker build and push") {
            agent { label: "docker" }
            steps {
                sh "docker version"
            }
        }
    }
}