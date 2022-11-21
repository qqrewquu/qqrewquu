pipeline{
  
  agent any 
  parameters{
    choice(name: 'VERSION',choices:['1.1.0','1.2.0','1.3.0'], description: '')
    booleanParam(name: 'executeTests', defaultValue: true, description: '' )

  }

  // access building tools for the project (maven, gradle, npm, etc)
  // tools{
  //     maven 'Maven'
  // }

  // define my own environmental variables
  // environment{
  //   NEW_VERSION = '1.3.0'
  //   SERVER_CREDENTIALS = credentials('server-credientals') // get credential from server
  // }
  
  stages{
    stage("build"){

      steps{
        echo 'building the applcation .....'
        // echo "building version ${NEW_VERSION}"
      }
    }
    stage("test"){
      when{
        expression{
          params.executeTests
        }
      }
      steps{
        echo 'testing the applcation .....'
      }
    }
    stage("deploy"){
      steps{
        echo 'deploying the applcation .....'
        echo "deplying version ${params.VERSION}"
        // echo "deploying with ${SERVER_CREDENTIALS}"
        // sh $"{SERVER_CREDENTIALS}"
      }
    }  
  }


  
}
