
pipeline {
    agent any

    stages {
        stage("github repo"){
            steps {
                git branch: 'main',credentialsId: 'gitcred',url: 'https://github.com/saitejat1907/RHEL.git'  // Cloning your GitHub repo
            }
        }
        // stage("Execute Ansible") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'Playbook/serviceaccount.yml'
        //     }
        // }
        // stage("Execute WebLogic Playbook") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'Playbook/weblogic.yml'
        //     }
        // }
        // stage("Execute WebLogic Deployment Playbook") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'Playbook/deployment.yml'
        //     }
        // }
        stage("Execute apache Playbook") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'Playbook/mysql.yml'
            }
        }
        // stage("Execute apache Playbook") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'Playbook/mysql2.yml'
        //     }
        // }
    }
}
