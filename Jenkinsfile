pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch: 'master', url: 'https://github.com/csah01/projCert'
            }
        }
        stage('Execute Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'privatekey', 
                disableHostKeyChecking: true, 
                installation: 'myansible', 
                inventory: 'dev.inv', 
                playbook: 'assignment.yml'
            }
        }
    }
}
