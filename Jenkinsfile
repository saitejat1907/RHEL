pipeline {
    agent any

    stages {
        stage("Ping All Hosts") {
            steps {
                ansibleAdhoc credentialsId: 'Ansible',
                               disableHostKeyChecking: true,
                               inventory: 'dev.inv',
                               command: 'all -m ping'
            }
        }
    }
}

