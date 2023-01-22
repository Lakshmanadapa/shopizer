pipeline {
    agent { label'OPEN' }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/Lakshmanadapa/shopizer.git',
                 branch: 'main'
            }
        }
        stage('openmrs build') {
            steps {
                sh 'mvn clean install'
            }
        }

    }
}