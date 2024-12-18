pipeline{

agent any
    environment{
        VERSION_NAME = "1.34"
    }

    stages{
        stage("compile"){
            steps{
                bat 'javac Main.java'
                bat 'echo "${VERSION_NAME}"'
            }

        }

        stage("run"){
            steps{
                bat "java Main"
            }
        }
    }

    post{

        always{
            bat 'echo "always"'
        }

        success{
            bat 'echo "success"'
        }

        failure{
            bat 'echo "failure"'
        }
    }


}