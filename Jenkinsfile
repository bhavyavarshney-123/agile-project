pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
             // bat "rmdir  /s /q agile-project"
                bat "git clone https://github.com/bhavyavarshney-123/agile-project.git"
                bat "mvn clean -f agile-project"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f agile-project"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f agile-project"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f agile-project"
            }
        }
    }
}
