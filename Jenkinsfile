pipeline {                                                    # All Jenkins pipeline files start with this line
  agent any                                                   # Agents where the file will run
  stages {                                                    # Stages of the CI/CD. The number os stages depends on the necessity
    stage ('Build') {                                         # Name of the stage.
      steps {                                                 # Steps necessary in order to complete the particular stage
        echo 'Running build automation'                       # What we want to do
        sh './gradlew build --no-daemon'                      # Shell step to execute a command line command. To run the build on Jenkins
        archiveArtifacts artifacts: dist/trainSchedule.zip    # Sending results to zip file
      }                                                       # gradlew is used to speed up builds, no recommended in pipelines. 
    }
  }
}
