### Changelog

### [0.2.3-alpha] - 2018-09-27
> NOTE: hastic-panels of versions older than 0.2.3 are not supported

#### Added
- More basic info about server [#154](https://github.com/hastic/hastic-server/issues/154)
- Integrate [grafana-datasource-kit](https://github.com/CorpGlory/grafana-datasource-kit) [#158](https://github.com/hastic/hastic-server/issues/158):
  - Graphite support
  - Prometheus support

#### Changed
- Reduce amount of required labeled segments for learning [#147](https://github.com/hastic/hastic-server/issues/147)

### [0.2.2-alpha] - 2018-09-12
> NOTE: hastic-panels of versions older than 0.2.0 are not supported

#### Changed
- Consider segment width in models [#136](https://github.com/hastic/hastic-server/issues/136)
- Increase learning dataset timerange

### [0.2.1-alpha] - 2018-09-04
> NOTE: hastic-panels of versions older than 0.2.0 are not supported

#### Changed
- Models improvements

### [0.2.0-alpha] - 2018-09-03
> NOTE: hastic-panels of versions older than 0.2.0 are not supported

#### Added
- Return version of server [#66](https://github.com/hastic/hastic-server/issues/66)
- Return analytic status [#71](https://github.com/hastic/hastic-server/issues/71)

#### Fixed
- Case-sensitive anomaly name [#41](https://github.com/hastic/hastic-server/issues/41)
- ImportError: cannot import name 'isna' [#59](https://github.com/hastic/hastic-server/issues/59)
- Handle analytics connection failure on server [#74](https://github.com/hastic/hastic-server/issues/74)
- Analytics wont start in production mode [#77](https://github.com/hastic/hastic-server/issues/77)
- Basic creation of analytic unit fails [#79](https://github.com/hastic/hastic-server/issues/79)
- Missing communication between analytics and server in production [#91](https://github.com/hastic/hastic-server/issues/91) - thx [@petrk94](https://github.com/petrk94) for [bugreport](https://github.com/hastic/hastic-server/issues/90)
- Server is stopping only after second Ctrl-C [#96](https://github.com/hastic/hastic-server/issues/96)
- Error: 'value' [#100](https://github.com/hastic/hastic-server/issues/100)
- Error: Unexpected response [#125](https://github.com/hastic/hastic-server/issues/125)
- Error: max of an empty sequence in peaks model [#126](https://github.com/hastic/hastic-server/issues/126)

### [0.1.4-alpha] - 2018-06-29
#### Changed
- Informative error messages instead of "Internal error" [#40](https://github.com/hastic/hastic-server/issues/33)

#### Fixed
- "No such file or directory" error on anomaly create [#33](https://github.com/hastic/hastic-server/issues/33)
- Case-sensitive anomaly name [#41](https://github.com/hastic/hastic-server/issues/41)

### [0.1.3-alpha] - 2018-06-28
#### Changed
- Drops algorithm improvement.

### [0.1.2-alpha] - 2018-06-25
#### Fixed
- Error: type object 'sklearn.tree...' [#28](https://github.com/hastic/hastic-server/issues/28)

### [0.1.1-alpha] - 2018-06-25
#### Added
- HASTIC_API_KEY to config file [#23](https://github.com/hastic/hastic-server/issues/23)