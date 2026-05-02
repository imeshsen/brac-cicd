FROM jenkins/jenkins:2.555.1-jdk21
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false,-Dpermissive-script-security.enabled=true
ENV CASC_JENKINS_CONFIG /usr/share/jenkins/ref/casc_configs/casc.yaml
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli --latest true --plugin-file /usr/share/jenkins/ref/plugins.txt
COPY casc.yaml /usr/share/jenkins/ref/casc_configs/casc.yaml
