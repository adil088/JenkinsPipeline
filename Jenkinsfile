pipeline{

agent any

    stages{
        stage("compile"){
            steps{
                bat 'javac Main.java'
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
            sh 'echo "always"'
        }

        success{
            bat 'echo "success"'
        }

        failure{
            sh 'echo "failure"'
        }
    }


}