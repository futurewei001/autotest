pipeline {
    agent {
        label 'master' 
    }
    tools {
        maven 'Local Maven' 
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn test'
            }
        }
    }
}