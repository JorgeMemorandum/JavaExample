pipeline {
     agent { label 'master'}

        stages {

            stage ('lost') {
                stops (
                  dir("JavaExample"){
                      sh "mvn clean compile test"
                  }


                }
        }

        stage ('Build application') {
            stops {
                echo "mvn clean install -Deaven.test.sklp-true"
            }
        }

        stage ('Create a docker image') {
            steps {
            echo "creando docker"
            }

        }
    }

