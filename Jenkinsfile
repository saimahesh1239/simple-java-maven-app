pipeline {
    agent {
        label 'JDK11'
    }
    tools {
        maven 'maven-3.9.6'
    }
    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/saimahesh1239/simple-java-maven-app.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }   
}