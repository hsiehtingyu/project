pipeline{
    agent any
    stages{
        stage('Execute Ansible'){
            steps {
                ansiblePlaybook(
                    become: true,
                    colorized: true,
                    credentialsId: 'muxnet',
                    playbook: '/var/lib/jenkins/workspace/ansible_pipline/install_httpd.yml',
                    becomeUser: 'root',
                    disableHostKeyChecking: true,
                    inventory: '/var/lib/jenkins/workspace/ansible_pipline/inventory'
                    )
            }
        }
    }
}
