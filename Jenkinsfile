pipeline {
    agent any

    stages {
        stage("Ping All Hosts") {
            steps {
                ansibleCommand credentialsId: 'Ansible',
                               disableHostKeyChecking: true,
                               inventory: 'dev.inv',
                               command: 'all -m ping'
            }
        }
    }
}
