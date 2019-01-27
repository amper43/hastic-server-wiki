### Changelog

### [0.2.7-alpha] - 2019-01-22

#### Added
- Threshold detector [#324](https://github.com/hastic/hastic-server/issues/324)
- Grafana url to config [#114](https://github.com/hastic/hastic-server/issues/114)
- Endpoint for setting analytic unit metric [#338](https://github.com/hastic/hastic-server/issues/338)
- Log all analytics errors [#353](https://github.com/hastic/hastic-server/issues/353)
- Endpoint for analytic unit types [#328](https://github.com/hastic/hastic-server/issues/328)

#### Fixed
- Webhooks [#341](https://github.com/hastic/hastic-server/pull/341)
- ElasticSearch scrolling [grafana-datasource-kit/#49](https://github.com/CorpGlory/grafana-datasource-kit/issues/49)
- Detection return empty result [#347](https://github.com/hastic/hastic-server/issues/347)
- Segments from data puller not in db and panel [#350](https://github.com/hastic/hastic-server/issues/350)
- TypeError: console.debug is not a function in node 6 [#360](https://github.com/hastic/hastic-server/issues/360)
- Error: '<' not supported between instances of 'NoneType' and 'NoneType' [#323](https://github.com/hastic/hastic-server/issues/323)
- IndexError: list index out of range if segment has NaN [#242](https://github.com/hastic/hastic-server/issues/242)
- Error: name 'parse_segment' is not defined [#315](https://github.com/hastic/hastic-server/issues/315)
- Error: ValueError - dataset input should have multiple elements [#325](https://github.com/hastic/hastic-server/issues/325)

#### Changed
- Move data cropping to the models [#335](https://github.com/hastic/hastic-server/issues/335)

### [0.2.6-alpha] - 2018-12-07

#### Added
- Verification of incoming and outgoing data in analytics [#227](https://github.com/hastic/hastic-server/issues/227)

#### Fixed
- Restore [webhooks](https://github.com/hastic/hastic-server/wiki/Webhooks) API [#149](https://github.com/hastic/hastic-server/issues/149)
- The center of drop and jump patterns is shifted from real value [#291](https://github.com/hastic/hastic-server/issues/291)
- No detections after fresh learning [#298](https://github.com/hastic/hastic-server/issues/298)

### [0.2.5-alpha] - 2018-12-03

#### Added
- PostgreSQL / TimescaleDB support (update [grafana-datasource-kit](https://github.com/CorpGlory/grafana-datasource-kit) to 0.0.11)
- Parallel learning for analytic units [#203](https://github.com/hastic/hastic-server/issues/203)

#### Fixed
- Cancel learning on analytic unit deletion [#266](https://github.com/hastic/hastic-server/issues/266)
- npm security alert: [GHSA-mh6f-8j2x-4483](https://github.com/dominictarr/event-stream/issues/116)
- Missing git info in Docker image [#238](https://github.com/hastic/hastic-server/issues/238)

### [0.2.4-alpha] - 2018-11-19
> NOTE: hastic-panels of versions older than 0.2.3 are not supported

#### Added
- Processing for 'NaN' values [#231](https://github.com/hastic/hastic-server/issues/231)

#### Changed
- Server info v2 [#167](https://github.com/hastic/hastic-server/issues/167)
- Specific error messages [#201](https://github.com/hastic/hastic-server/issues/201)
- Models with filtering [#186](https://github.com/hastic/hastic-server/issues/186)
- Decouple "analytics" and "server" processes to different docker containers [#187](https://github.com/hastic/hastic-server/issues/187)

#### Fixed
- Fix models for choosing the "wrong" patterns [#195](https://github.com/hastic/hastic-server/issues/195)
- Old segments are not deleted [#198](https://github.com/hastic/hastic-server/issues/198)
- Analytics works with one labeled segment [#191](https://github.com/hastic/hastic-server/issues/191)
- Error list index out of range AND max() arg is an empty sequence [#212](https://github.com/hastic/hastic-server/issues/212)
- Incorrect work of models with single patterns [#234](https://github.com/hastic/hastic-server/issues/234)
- Incorrect work of analytics with NaN-filled dataset [#247](https://github.com/hastic/hastic-server/issues/247)
- Anti-segments do not fall into analytics [#181](https://github.com/hastic/hastic-server/issues/181)

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