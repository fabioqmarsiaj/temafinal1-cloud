pipeline {
   agent any
    stages {
        stage('Git') {
            steps {
               git url: 'https://github.com/fabioqmarsiaj/temafinal1-cloud'
            }
        }
        stage('Build') {
            steps {
                sh('./gradlew clean build')
            }
        }
        stage('Jfrog') {
            steps {
                sh('curl -uadmin:AP5jYGTMVLpZepNRDHnMuuWD1H2 -T build/libs/temafinal1-cloud-0.0.1-SNAPSHOT.jar "http://localhost:8081/artifactory/example-repo-local/app.jar"')
            }
        }
    }
}