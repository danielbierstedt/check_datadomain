# check_datadomain
check_datadomain script for Icinga2

## Getting Started

Just put that script into the directory that contains your check scripts, plugins etc.

### Prerequisites

Several things need to be done on Data Domain to get this going. First, you need to set up SNMP V2c. Second, you need to set up SSH so the Icinga user can SSH to the Data Domain without a password.

## Running the checks

### repl_behind

This checks how far a replication is behind. Assume, there is a replication set up from one Data Domain onto another. You might want to know how far the replicaion is, or the other way around, how much is missing. This check uses the Data Domain predicion to guess how long it would take to get everything up2date. The result is expressed in seconds.

### repl_perf

This is about replication performance, the result is KB/s.

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
