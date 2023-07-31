pipeline {
   agent {
    label 'linux'
   }
    stages {
        stage('Prepare') {
            steps {
                sh "rm -rf vector-role"
                sh "git clone -b master git@github.com:vitaliy495/vector-role.git "
                sh "docker pull docker.io/pycontribs/centos:7"
                sh "docker pull docker.io/pycontribs/ubuntu:latest"
            }
        }
        stage('Test') {
            steps {
                dir('vector-role') {
                    sh "molecule test"
                }
            }
        }
    }
}