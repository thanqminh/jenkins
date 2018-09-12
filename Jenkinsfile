#!/usr/bin/env groovy
@Library('jenkins-pipeline-library@develop')



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


