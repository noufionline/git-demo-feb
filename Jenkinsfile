pipeline
{
  agent { node { label 'master'} }
  parameters {
    string(name: 'FileName', defaultValue:'', description: 'Please supply filename')
    choice(name: 'FileList', choices: ['demo.txt','ajay.txt'],description: 'Pick File')
  }
  
  stages{
    stage('Read demo file'){
      steps {
        sh "cat ${params.FileName}"
      }
    }
    stage('Read README.md file'){
      steps{
        sh 'cat README.md'
      }
    }
    stage('Read from choice'){
      steps{
        sh "cat ${params.FileList}"
      }
    }
  }
}
