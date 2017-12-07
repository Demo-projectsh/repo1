#!/usr/bin/env groovy
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/Demo-projectsh/repo1.git'],
    pipelineTriggers([
    		upstream(
		threshold: 'SUCCESS',
		upstreamProjects: 'https://github.com/Demo-projectsh/repo2.git'
	)])
])

pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'pwd' 
            }
        }
        stage('Test'){
            steps {
                sh 'java -version'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
                sh 'pwd'
            }
        }
    }
}
