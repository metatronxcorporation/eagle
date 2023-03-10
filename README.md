# Apache Eagle

>  The intelligent monitoring and alerting solution instantly analyzes big data platforms for security and performance

Apache® Eagle™ is an open source analytics solution for identifying security and performance issues instantly on big data platforms e.g. Apache Hadoop, Apache Spark, NoSQL etc. It analyzes data activities, yarn applications, jmx metrics, and daemon logs etc., provides state-of-the-art alert engine to identify security breach, performance issues and shows insights.

For more details, please visit [https://eagle.apache.org](https://eagle.apache.org)

[![Build Status](https://builds.apache.org/buildStatus/icon?job=incubator-eagle-main)](https://builds.apache.org/job/incubator-eagle-main/) 
[![Coverage Status](https://coveralls.io/repos/github/apache/incubator-eagle/badge.svg)](https://coveralls.io/github/apache/incubator-eagle)

## Documentation

You can find the latest Eagle documentation on [https://eagle.apache.org](https://eagle.apache.org/docs). This [README](README.md) file only contains basic setup instructions.

## Downloads

* Latest Release
    * [eagle-0.5.0](http://eagle.apache.org/docs/download-latest.html)
* Archived Releases
    * [eagle-0.4.0-incubating](http://eagle.apache.org/docs/download.html#0.4.0-incubating)
    * [eagle-0.3.0-incubating](http://eagle.apache.org/docs/download.html#0.3.0-incubating)
    * [More releases](http://eagle.apache.org/docs/download.html)

## Getting Started

### Prerequisites

* [JDK 8](https://jdk8.java.net/): Java Environment `Version 1.8`
* [Apache Maven](https://maven.apache.org/): Project management and comprehension tool `Version 3.x`
* [NPM](https://www.npmjs.com/): Node package management tool `Version 3.x`

### Building Eagle 

> Since version 0.5, Eagle is only built on JDK 8.

Eagle is built using [Apache Maven](https://maven.apache.org/). NPM should be installed (On MAC OS try "brew install node"). To build Eagle, run:
    
    mvn clean package -DskipTests 

After successfully building, you will find eagle binary tarball at:
    
    eagle-assembly/target/eagle-${VERSION}-bin.tar.gz

### Testing Eagle 

    mvn clean test

### Developing Eagle

* (Optional) Install/Start [HDP Sandbox](http://hortonworks.com/products/sandbox/) which provide an all-in-one virtual machine with most dependency services like Zookeeper, Kafka, HBase, etc and monitored hadoop components.
* Import Eagle as maven project with popular IDE like [IntelliJ IDEA](https://www.jetbrains.com/idea/)
* Start **Eagle Server** in `debug` mode by running (default http port: `9090`, default smtp port: `5025`)

        org.apache.eagle.server.ServerDebug
  
  Which will start some helpful services for convenient development:
  * Local Eagle Service on [`http://localhost:9090`](http://localhost:9090)
  * Local SMTP Service on `localhost:5025` with REST API at [`http://localhost:9090/rest/mail`](http://localhost:9090/rest/mail)
* Start **Eagle Apps** with Eagle Web UI in `LOCAL MODE`.

## Getting Help

* **Mail**: The fastest way to get response from eagle community is to send email to the mail list [dev@eagle.apache.org](mailto:dev@eagle.apache.org),
and remember to subscribe our mail list via [dev-subscribe@eagle.apache.org](mailto:dev-subscribe@eagle.apache.org)
* **Slack**: Join Eagle community on Slack via [https://apacheeagle.slack.com](https://apacheeagle.slack.com)
* **JIRA**: Report requirements, problems or bugs through apache jira system via [https://issues.apache.org/jira/browse/EAGLE](https://issues.apache.org/jira/browse/EAGLE)

## FAQ

[https://cwiki.apache.org/confluence/display/EAG/FAQ](https://cwiki.apache.org/confluence/display/EAG/FAQ)

## Contributing

Please review the [Contribution to Eagle Guide](https://cwiki.apache.org/confluence/display/EAG/Contributing+to+Eagle) for information on how to get started contributing to the project.

## License

Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0). More details, please refer to [LICENSE](LICENSE) file.
