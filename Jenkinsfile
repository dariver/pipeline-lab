node('cloud&&ubuntu') {
  withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'credentials-id',usernameVariable: 'USERNAME',passwordVariable: 'PASSWORD']]) { 
    sh 'echo $USERNAME $PASSWORD > OUT'
  }
  def value = readFile('OUT').trim()
  println value
}
