pipeline {
    agent { label 'ansible' }
    stages {
        stage('Git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/ashwini9921/Project1.git'
            }
        }
        stage('Ansible ping') {
            steps {
                sh "ansible all -i Project1/hosts -m ping"
            }
        }
        stage('Ansible playbook') {
            steps {
                sh "ansible-playbook -i Project1/hosts Project1/tomcat.yml"
            }
        }
    }
}

