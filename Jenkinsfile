pipeline {
    agent { label 'JDK' }
    triggers { pollSCM('* * * * *') }
    tools {
        maven 'Maven'
        }
    stages {
        stage('vcs') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/CAESAR269/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
      
    }
}
