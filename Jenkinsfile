pipeline {
    agent any
    tools {
       maven 'MAVEN_HOME'
       jdk 'JAVA_HOME'
    }

    stages {

        stage('Git Checkout'){

            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Bneeruga/springboot-session-management-master.git']])
            }
        }
        stage('UNIT Test'){

            steps{
            echo "PATH = ${PATH}"
            echo "M2_HOME = ${M2_HOME}"
             sh 'mvn test'
            }
        }

    }



}