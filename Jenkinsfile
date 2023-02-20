pipeline {
    agent any

    stages {

        stage('Git Checkout'){

            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Bneeruga/springboot-session-management-master.git']])
            }
        }
        stage('UNIT Test'){

            steps{
             sh 'mvn test'
            }
        }

    }



}