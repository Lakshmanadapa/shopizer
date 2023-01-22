pipeline {
    agent { label'OPEN' }
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