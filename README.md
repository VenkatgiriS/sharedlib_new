Pipeline Script for private Repo
library identifier: 'pipeline_call@main',
    // 'mylibraryname' is just an identifier, it can be anything you like
    // 'master' refers to a valid git ref (branch)
    retriever: modernSCM([
      $class: 'GitSCMSource',
      credentialsId: 'github', // remove this if it's public!
     // remote: 'https://github.com/VenkatgiriS/shalib_new.git'
      remote: 'https://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@github.com/VenkatgiriS/shalib_new.git'
      
])

pipeline {
    agent any
    stages {
        stage('Demo') {
            steps {
                echo 'Hello world'
                sayHello 'Venkat'
            }
        }
    }
}
