pipeline {
    agent any
    stages {
        stage('Git clone') {
            steps {
                git credentialsId: 'a3d89905-d6cc-4441-9cc3-568a428e17bf', url: 'git@github.com:arhipovea/ansible-role-nginx.git'
            }
        }
        stage('Molecule test') {
            steps {
                sh 'pip3 install --user "molecule" "molecule-docker"'
                sh 'molecule test'
            }
        }
    }
}