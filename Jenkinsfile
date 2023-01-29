#!/usr/bin/env groovy
//@Library('Jenkins-Shared-Library')
def gv

pipeline {
    agent any
    tools {
    maven 'Maven'
    }
    stages {
        stage("build jar") {
            steps {
                script {
                    buildJar()
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building image This is Jenkins file"
                    buildImage 'waseemkhandocker/my-docker-repo:java-package2-maven-app-from-shared-5.0'
                    dockerLogin()
                    dockerPush 'waseemkhandocker/my-docker-repo:java-package2-maven-app-from-shared-5.0'
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    //gv.deployApp()
                }
            }
        }
    }   
}
