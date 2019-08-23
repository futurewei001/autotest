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
                 step([$class: 'XrayImportBuilder', endpointName: '/junit', importFilePath: './target/surefire-reports/TEST-com.example.javamavenjunithelloworld.Demo1Test.xml', importToSameExecution: 'true', projectKey: 'TES', serverInstance: '68ac51bc-bfeb-4183-9bac-6916af76ca31'])
            }
           
        }
    }
}
