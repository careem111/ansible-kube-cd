pipeline{
    agent any

        parameters{
        string(name: 'ansible_server', defaultValue: '172.31.42.119', description: 'docker Server')
    }

    stages{
        stage('run ansible-playbook for kube deployment'){
            steps{
                sh """ssh 172.31.42.119 << EOF
                ansible-playbook ansible-kube-deploy.yaml
                ansible-playbook ansible-kube-service.yaml
                exit
                EOF"""

            }
    }

}
}
