flag=true
pipeline{
  agent any
  environment{
     NEW_VERSION= '1.3.0'
}

  stages{
    stage('Build'){
      steps{
        
        echo "this is build stage and here i am telling version ${NEW_VERSION}"
      }
    }
    stage('Test'){
      when{
          expression{
            flag==false
          }
      }
      steps{
      echo 'this is test stage'
    }
    }
    stage('Deploy'){
      steps{
        echo 'this is deploy stage'
      }
    }
  }
  

  post{
    always{
      echo 'it will run always'
    }
    failure{
      echo 'it will run if build fails'
    }
  }
}
    
