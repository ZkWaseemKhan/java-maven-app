#!/usr/bin/env groovy
@Library('Jenkins-Shared-Library')
 def gv

pipeline {
    agent any
    stages {
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    buildApp()
                    //gv.buildJar()
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building image"
                    //gv.buildImage()
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
