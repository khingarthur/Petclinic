pipeline {
    agent any

    stages{
    stage('Git checkout'){
        steps{
            checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/khingarthur/Petclinic.git']])        }
    }

    stage('Validate'){
        steps{
            sh 'mvn validate'
            }
        }

    stage('Compile'){
        steps{
            sh 'mvn -version'
            sh 'mvn compile'
        }
    }

     stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
     stage('List'){
            steps{
                sh 'ls'
            }
        }

	}
}
