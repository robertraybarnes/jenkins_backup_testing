pipeline {
  agent any
  stages {
    stage('esxi_provision') {
      parallel {
        stage('esxi_provision') {
          steps {
            build 'esxi_provision'
          }
        }
        stage('appliance_provision') {
          steps {
            build 'appliance_provison'
          }
        }
        stage('appliance_testing_prep') {
          steps {
            build 'appliance_testing_prep'
          }
        }
        stage('appliance_testing') {
          steps {
            build 'appliance_testing_prep'
          }
        }
      }
    }
  }
}