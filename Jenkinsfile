pipeline {
    
    agent any 
            stages{
                stage('Build'){
                    steps{
                        sh 'mvn clean package'
                    }
                    post {
                        sucess {
                            echo 'Archiving artifacts'
                            archiveArtifacts artifacts: '**/target/*.war'
                        }
                    }
                }
                stage('build'){
                    steps{
                        echo('hello build stage')
                    }
                }

                stage('deploy'){
                    steps{
                        echo('Hello deployement')
                    }
                } 
            }

    }