pipeline {
    agent {
        node{
            label 'maven-agent'
        }
    }

    stages {
        stage('Clone code') {
            steps {
                git 'https://github.com/kamlesh1905/ttrendnew01.git'
            }
        }
    }
}