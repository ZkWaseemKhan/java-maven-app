#!/usr/bin/env groovy
@Library('Jenkins-Shared-Library')
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
                    echo "building image"
                    buildImage 'waseemkhandocker/my-docker-repo:java-package-maven-app-from-shared-5.0'
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
