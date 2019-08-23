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
                sh "curl -H \"Content-Type: multipart/form-data\" -u annie.yau:technet@1234 -F \"file=@./target/surefire-reports/TEST-com.example.javamavenjunithelloworld.Demo1Test.xml\" http://13.94.39.23:8080/rest/raven/1.0/import/execution/junit?projectKey=TES"
            }
        }
    }
}
