pipeline {
  agent none
  stages {
    stage('begin') {
      steps {
        node(label: 'centos') {
          sh '''#!/bin/bash

echo "testing"'''
          sleep 10
        }
        
      }
    }
  }
}