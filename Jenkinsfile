pipeline {
    agent any
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
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}