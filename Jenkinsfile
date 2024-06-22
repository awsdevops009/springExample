pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                sh 'rm -rf springExample'
                sh 'git clone https://github.com/awsdevops009/springExample.git'
                sh 'mvn clean'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -f springExample/pom.xml'
                echo 'Welcome to Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package -f springExample/pom.xml'
                echo 'It is going to package the project today'
            }
        }
    }
}
