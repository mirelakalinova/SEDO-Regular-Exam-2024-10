pipeline {
    agent any 

    
        stage('Build') {
            steps {
               
                bat 'dotnet build'
            }
        }

      stage('Run Unit Tests') {
            steps {
               
                bat 'dotnet test HouseRentingSystem.Tests/HouseRentingSystem.Tests.csproj --no-build --verbosity normal'
            }

        stage('Run Integration Tests') {
            steps {
               
                bat 'dotnet test HouseRentingSystem.UnitTests/HouseRentingSystem.UnitTests.csproj --no-build --verbosity normal'
            }
       
        }
    }
}
