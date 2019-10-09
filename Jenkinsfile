#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Initialise') {
            steps {
                sh "rm -rf sdu-related"
                sh 'git clone https://github.com/PaulBroughton/sdu-related.git'
            }
        }
        stage('Build') {
            steps {
                sh 'packer version'
                sh 'ansible --version'
                sh 'terraform version'
                sh 'docker version'
                sh 'make --version'
                sh 'kubectl --help'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
