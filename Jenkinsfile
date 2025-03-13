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
        stage("github repo"){
            steps {
                git branch: 'main',url: 'https://github.com/saitejat1907/RHEL.git'  // Cloning your GitHub repo
            }
        }
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
