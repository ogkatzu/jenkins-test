@library('shared-library') _

pipeline{
    agent{
        any
    }
    stages{
        stage("Stage A"){
            steps{
                echo "========executing A========"
                sh 'hostname'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
        stage("Stage B"){
            steps{
                echo "========executing B========"
                helloWorld([name: 'Saar'])
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========B executed successfully========"
                }
                failure{
                    echo "========B execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}