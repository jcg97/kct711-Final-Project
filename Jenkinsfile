node {
  stage ('Build') {
    withMaven {
      bat "mvn -B -DskipTests clean package"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}