node {
  stage ('Build') {
    git url: 'https://github.com/jcg97/kct711-Final-Project'
    withMaven {
      sh "mvn -B -DskipTests clean package"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}