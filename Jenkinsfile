// pipeline {
//     agent any

//     stages {
//         stage("Ping All Hosts") {
//             steps {
//                 ansibleAdhoc credentialsId: 'Ansible',
//                                disableHostKeyChecking: true,
//                                inventory: 'dev.inv',
//                                command: 'all -m ping'
//             }
//         }
//     }
// }

pipeline {
    agent any

    stages {
        stage("Execute Ansible") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/serviceaccount.yml'
            }
        }
    }
}
