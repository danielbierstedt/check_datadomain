# check_datadomain
check_datadomain script for Icinga2

## Getting Started

Just put that script into the directory that contains your check scripts, plugins etc.

### Prerequisites

Several things need to be done on Data Domain to get this going. First, you need to set up SNMP V2c. Second, you need to set up SSH so the Icinga user can SSH to the Data Domain without a password.

## Running the checks

### repl_behind

This checks how far a replication is behind. Assume, there is a replication set up from one Data Domain onto another. You might want to know how far the replicaion is, or the other way around, how much is missing. This check uses the Data Domain predicion to guess how long it would take to get everything up2date. The result is expressed in seconds.

```
./check_datadomain -H HOST -r MTREE -t repl_behind -w 86400 -c 172800 -d DESTINATION
```

### repl_perf

This is about replication performance, the result is KB/s.

```
./check_datadomain -H HOST -t repl_perf -w 40 -c 30 -r MTREE -d DESTINATION
```

### quota
Checking quota of an Mtree by SNMP. Getting the hard quota value and calculating from there.
```
./check_datadomain -H HOST -t quota -w 70 -c 80 -m MTREE
```

## Versioning

We use [SemVer](http://semver.org/) for versioning.

## Authors

* **Daniel Bierstedt**

## License

This project is licensed under the GPLV3 License - see the [LICENSE.md](LICENSE.md) file for details

