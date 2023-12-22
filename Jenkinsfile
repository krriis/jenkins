pipeline {
    agent any
    environment {
       dotnet = '"C:\\Program Files\\dotnet\\dotnet.exe"'
    }


    stages {
       
          stage('Build') {
                steps {
                   dir("PrimeService.Tests"){
                    bat "${dotnet} build"
                   }
                }
            }

            stage('Testing') {
                steps {
                   dir("PrimeService.Tests"){
                    bat "${dotnet} test"
                   }
                }
            }

            stage('Cleanimng') {
                steps {
                   dir("PrimeService.Tests"){
                    bat "${dotnet} clean"
                   }
                }
            }

    }
}