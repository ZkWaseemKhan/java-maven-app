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
                    buildImage 'waseemkhandocker/my-docker-repo:java-maven-app-from-shared-4.0'
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
