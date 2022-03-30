pipeline {
     agent any
    tools{
        jdk 'jdk11'
        maven 'maven'
         }

    stages {

        stage('Build') {
            steps {
                sh 'java --version'
                sh 'echo $JAVA_HOME'
                sh 'mvn -B -DskipTests clean package'

            }
        }

        stage('Run') {
            steps {
                sh returnStdout: true, script: 'java -jar  target/netflix-1.0.0.jar  netflix_titles.csv'

                }
            }
          }

}