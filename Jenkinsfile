pipeline {
  agent any
  stages {
    stage('Licenses Checks') {
      steps {
        git(url: 'https://github.com/AntonioFantini/example_product.git', branch: 'master')
        load './checks/LicenseChecks.groovy'
      }
    }
  }
}