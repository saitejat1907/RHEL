pipeline {
    agent any
    stages {
        stage('Run Ansible') {
            steps {
                sh 'ansible all -m ping'
            }
        }
    }
}
