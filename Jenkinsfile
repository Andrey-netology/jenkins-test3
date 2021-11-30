pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('Checkout') {
            steps{
                git branch: 'main', credentialsId: '9d5feaa5-99e4-478e-86d1-e0c60624459d', url: 'git@github.com:Andrey-netology/jenkins-test3.git'
            }
        }
        stage('Install molecule') {
            steps{
                sh 'pip3 install -r test-requirements.txt'
                sh "echo =============="
            }
        }
        stage('Run Molecule'){
            steps{
                sh 'molecule test'
            }
        }
    }
}
