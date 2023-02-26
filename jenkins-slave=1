pipeline {
    agent {lebel 'jenkins-slave-1'}
    stages {
        stage('Build') {
            steps {
                sh "rm -rf springExample"
                sh "git clone https://github.com/awsdevops009/springExample.git"
                sh "mvn clean -f springExample"
                echo ' job finished'
            }
        }
    }
}
