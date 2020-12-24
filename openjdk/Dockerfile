from hanlinyang/ubuntu:20.04

# Install AdoptOpenJDK 11 (from official repository) and Maven (from Ubuntu repository)
# Maven from Ubuntu focal repository is new enough
RUN apt-get update && apt-get install -y \
    apt-transport-https gnupg \
 && (wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | apt-key add -) \
 && (echo "deb https://adoptopenjdk.jfrog.io/adoptopenjdk/deb focal main" | tee /etc/apt/sources.list.d/adoptopenjdk.list) \
 && apt-get update \
 && apt-get install -y adoptopenjdk-11-hotspot \
    maven \
 && rm -rf /var/lib/apt/lists/*

 # Set up Aliyun Maven mirror
 COPY ./openjdk/settings.xml /usr/share/maven/conf/settings.xml
