pipeline {
  agent any
  node () {

	stage ('scm - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '1803.00']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '1a29df34-35c4-44f3-8017-0e854fac0963', url: 'https://github.com/SMEStorage/devops']]]) 
	}
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
