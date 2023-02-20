pipeline {
    agent any
    tools{
        maven 'Maven 3.9.0'
        jdk 'jdk8'
    }

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