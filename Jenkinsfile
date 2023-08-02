pipeline {
    agent any
    
    stages {
        stage('MVN PACAKAGE') {
            steps {
                sh '''export M2_HOME=/opt/maven
                export MAVEN_HOME=/opt/maven
                export PATH=${M2_HOME}/bin:${PATH}
                mvn clean install
                sleep 10
                cd target/
                java -jar jb*.jar'''
            }
        }
        
        stage('DEPLOYMENT IS SUCCESS') {
            steps {
                sh 'sleep 10'
            }
        }
    }
}
