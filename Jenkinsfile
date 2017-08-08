pipeline {
  agent any
  stages {
    stage('Licenses Checks') {
      steps {
        git(url: 'https://github.com/AntonioFantini/pipeline-tools.git', branch: 'master')
        load './checks/LicenseChecks.groovy'
      }
    }
    stage('Crypto Checks') {
      steps {
        load './checks/CryptoChecks.groovy'
      }
    }
    stage('CVE Checks') {
      steps {
        load './checks/CVEChecks.groovy'
      }
    }
    stage('Dependency Checks') {
      steps {
        load './checks/DependencyChecks.groovy'
      }
    }
  }
}