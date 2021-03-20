pipeline{
 
  agent any
  
  stages{
  stage("run frontend"){
      steps{
        echo 'executing yarn...'
       nodejs('Node-10.17'){
         sh 'yarn intall'
       }
      }
    }
  
    stage("run backend"){
      steps{
        echo 'executing gradle..'
       withGradle(){
         sh './gradlew -v'
       }
      }
    }
 
    stage("build"){
      steps{
        echo 'building application...'
      }
    }
  
    stage("test"){
      steps{
        echo 'testing application...'
      }
    }
  

    stage("deploy"){
      steps{
        echo 'deploying application...'
         }
    }
  }
}

//node{
 //groovy script based pipelining
//}
