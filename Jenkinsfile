#!/usr/bin/env groovy
@Library('jenkins-pipeline-library@develop')


try {
    def environment = null

    node {
        stage("Prepare environment") {
            checkout scm
        }

        stage("list files") {
             sh 'ls'
        }
        stage("Build Docker container") {
             environment = docker.build("wingo-tyke:latest")
        }

    }
    currentBuild.result = 'SUCCESS'
} catch (e) {
    currentBuild.result = 'FAILURE'
    throw e
}


