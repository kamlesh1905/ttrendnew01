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
                sh 'mvn clean deploy'
               echo "----------- build complted ----------"
            }
        }
}
    stage('SonarQube analysis') {
        environment {
         scannerHome = tool 'SonarScannner'
        }
        steps{
        withSonarQubeEnv('SonarQube-Server') { // If you have configured more than one global server connection, you can specify its name
        sh "${scannerHome}/bin/sonar-scanner"
     }
    }
   }

}