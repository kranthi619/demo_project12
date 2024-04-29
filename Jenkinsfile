pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/kranthi619/demo_project12.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook(
                    credentialsId: '5b92bfea-ee25-489e-9470-549ced627ffd',
                    disableHostKeyChecking: true,
                    installation: 'ansible',
                    inventory: 'dev.inv',
                    playbook: 'copy.yml'
                )
            }
        }
    }
}
