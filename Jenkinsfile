#!/usr/bin/env groovy Jenkinsfile
node{
    def gradleHome = tool 'Gradle4.7'
    env.PATH = "${gradleHome}/bin:${env.PATH}"
}
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'gradle build --info'
            }
        }
        stage('Test') {
            steps {
                sh 'gradle test --info'
            }
        }

    }
}
