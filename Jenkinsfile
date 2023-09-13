pipeline {
    agent {
        node{
            label 'maven-agent'
        }
    }
	environment {
    PATH = "/opt/apache-maven-3.9.4/bin:$PATH"
}
    stages {
        stage('build') {
            steps {
               echo "----------- build started now ----------"
                sh 'mvn clean deploy
               echo "----------- build complted ----------"
            }
        }
}

}