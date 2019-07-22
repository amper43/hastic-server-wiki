### Changelog

### [0.4.0] - not released yet
#### Changed
- Anomaly detector bounds switch: disabling to enabling [#709](https://github.com/hastic/hastic-server/issues/709)

#### Fixed
- Data kit error: status code 400 [#300](https://github.com/hastic/hastic-server/issues/300)
- Don't throw exception if HASTIC_WEBHOOK_URL is undefined [#593](https://github.com/hastic/hastic-server/issues/593)

### [0.3.6-beta] - 2019-07-04
#### Added
- Anomaly detector: option for disabling upper / lower bound [#701](https://github.com/hastic/hastic-server/issues/701)
- Segment info [#693](https://github.com/hastic/hastic-server/issues/693)
- "[PATTERN DETECTED]" in webhooks message [#560](https://github.com/hastic/hastic-server/issues/560)
- Image for webhook [#705](https://github.com/hastic/hastic-server/issues/705)

#### Fixed
- Error: Request failed with status code 406 [#605](https://github.com/hastic/hastic-server/issues/605)

### [0.3.5-beta] - 2019-06-04
#### Fixed
- Error: Cannot read property 'alpha' of null [#687](https://github.com/hastic/hastic-server/pull/687)
- Anomaly detector: NaN as last value [#677](https://github.com/hastic/hastic-server/issues/677)
- Anomaly detector: swapped upper / lower bounds [#683](https://github.com/hastic/hastic-server/issues/683)
- Error "Can't find interval: length of data" [#688](https://github.com/hastic/hastic-server/pull/688)

#### Changed
-  Name for basic anomaly detector type [#663](https://github.com/hastic/hastic-server/issues/663)

### [0.3.4-beta] - 2019-05-20
#### Added
- HSR for anomaly analytic unit [#653](https://github.com/hastic/hastic-server/issues/653)
- Labeling for anomalies [#631](https://github.com/hastic/hastic-server/issues/631)
- HASTIC_PORT in .env file [#640](https://github.com/hastic/hastic-server/issues/640)

#### Fixed
- Thresholds error: from is NaN [#621](https://github.com/hastic/hastic-server/issues/621)
- Anomaly detector: Need at least 1 labeled segment [#667](https://github.com/hastic/hastic-server/issues/667)
- Queue or drop learning task on new learning task [#664](https://github.com/hastic/hastic-server/issues/664)
- Anomaly detector: wrong seasonality offset [#671](https://github.com/hastic/hastic-server/issues/671)
- Not ending learning for anomaly detector [#665](https://github.com/hastic/hastic-server/issues/665)

#### Changed
- Detect thresholds on the whole dataset instead of 1 value [#505](https://github.com/hastic/hastic-server/issues/505)
- Start learning after analytic unit update [#647](https://github.com/hastic/hastic-server/issues/647)
- Set ready status for span only after inserting segments [#648](https://github.com/hastic/hastic-server/issues/648)
- Remove old detected segments and detection spans when learning starts [#650](https://github.com/hastic/hastic-server/issues/650)
- Merge threshold segments [#624](https://github.com/hastic/hastic-server/issues/624)
- Remove old detected segments and detection spans when learning starts [#650](https://github.com/hastic/hastic-server/issues/650)
- Anomaly detector: send confidence bounds instead of smoothed data [#656](https://github.com/hastic/hastic-server/issues/656)

### [0.3.3-beta] - 2019-04-24

#### Added
- Detection in selected time range [#504](https://github.com/hastic/hastic-server/issues/504)
- Endpoint for getting timeseries of analytic unit [#528](https://github.com/hastic/hastic-server/issues/528)
- Webhooks: Hastic instance name / url [#547](https://github.com/hastic/hastic-server/issues/547)

#### Fixed
- Analytic's dependencies size [#540](https://github.com/hastic/hastic-server/issues/540)
- Don't run detection if learning failed [#549](https://github.com/hastic/hastic-server/issues/549)
- ValueError: array must not contain infs or NaNs [#563](https://github.com/hastic/hastic-server/issues/563)
- Dataframe for detection less than two window size [#531](https://github.com/hastic/hastic-server/issues/531)
- RPM: Hastic server has unsupported version [#557](https://github.com/hastic/hastic-server/issues/557)

#### Changed
- Sort analytic units by creation date / name [#514](https://github.com/hastic/hastic-server/issues/514)
- Check python version in run time [#592](https://github.com/hastic/hastic-server/issues/592)

### [0.3.2-beta] - 2019-04-08

#### Added
- Learning timeout [#481](https://github.com/hastic/hastic-server/issues/481)
- Server info: number of task resolvers [#510](https://github.com/hastic/hastic-server/pull/510)
- Server info: Detections number [#516](https://github.com/hastic/hastic-server/pull/516)
- Hastic-exporter for Prometheus [#520](https://github.com/hastic/hastic-server/pull/520)

#### Changed
- Synchronization with panel [#455](https://github.com/hastic/hastic-server/issues/455)
- Add tasks to queue when analytics is not ready [#468](https://github.com/hastic/hastic-server/issues/468)
- Send data to detection in chunks [#489](https://github.com/hastic/hastic-server/issues/489)
- Batch detection [#500](https://github.com/hastic/hastic-server/issues/500)
- Find start and end of peaks and troughs [#506](https://github.com/hastic/hastic-server/issues/506)

#### Fixed
- Not-ending learning [#264](https://github.com/hastic/hastic-server/issues/264)
- Analytic units' panel fields are not saved to db [#523](https://github.com/hastic/hastic-server/issues/523)
- KeyError: 'pattern_model' [#471](https://github.com/hastic/hastic-server/issues/471)
- Prometheus returns wrong time units [CorpGlory/grafana-datasource-kit#62](https://github.com/CorpGlory/grafana-datasource-kit/issues/62)
- ValueError: attempt to get argmin of an empty sequence [#518](https://github.com/hastic/hastic-server/issues/518)

### [0.3.1-beta] - 2019-03-05

#### Fixed
- TypeError: ufunc 'isnan' not supported for the input types [#447](https://github.com/hastic/hastic-server/issues/447)
- Analytic bucket size [#446](https://github.com/hastic/hastic-server/issues/446)

### [0.3.0-beta] - 2019-02-26

#### Added
- Webhook about missing connection to Grafana [#412](https://github.com/hastic/hastic-server/issues/412)
- Accept various URL inputs [#416](https://github.com/hastic/hastic-server/issues/416)
- Print config options on start [#365](https://github.com/hastic/hastic-server/issues/365)
- More info in webhooks [#436](https://github.com/hastic/hastic-server/pull/436)
- Accept various URL inputs [#416](https://github.com/hastic/hastic-server/issues/416)
- RPM release [#317](https://github.com/hastic/hastic-server/pull/317)

#### Fixed
- KeyError: 'ipeaks' [#410](https://github.com/hastic/hastic-server/issues/410)
- Drops pattern ValueError: All elements of patterns_list should have same length [#414](https://github.com/hastic/hastic-server/issues/414)
- ValueError: operands could not be broadcast together with shapes [#425](https://github.com/hastic/hastic-server/issues/425)
- Do not insert found segment if it intersects with negative [#434](https://github.com/hastic/hastic-server/issues/434)
- No server info [#417](https://github.com/hastic/hastic-server/issues/417)
- Disable webhook: TypeError: Cannot read property 'toString' of undefined [#415](https://github.com/hastic/hastic-server/issues/415)
- UnhandledPromiseRejectionWarning [#419](https://github.com/hastic/hastic-server/issues/419)

#### Changed
- Pattern filtering logic [#366](https://github.com/hastic/hastic-server/issues/366)
- Add correlation in general model [#437](https://github.com/hastic/hastic-server/issues/437)

### [0.2.8-alpha] - 2019-02-11

#### Added
- Renaming of analytic units [#343](https://github.com/hastic/hastic-server/issues/343)

#### Fixed
- Empty config value is not replaced by default value [#380](https://github.com/hastic/hastic-server/issues/380)
- Error: cannot read property `analyticUnitId` of undefined [#378](https://github.com/hastic/hastic-server/issues/378)
- Setting `GRAFANA_URL` in .env doesn't work [#376](https://github.com/hastic/hastic-server/issues/376)
- Nonetype object has no attribute update [#375](https://github.com/hastic/hastic-server/issues/375)
- Threshold value is not saving [#368](https://github.com/hastic/hastic-server/issues/368)
- Sort segments in `processDetectionResult` [#354](https://github.com/hastic/hastic-server/issues/354)
- Thresholds work incorrect with elastic datasource [#388](https://github.com/hastic/hastic-server/issues/388)
- KeyError 45058 [#389](https://github.com/hastic/hastic-server/issues/389)
- Error: missing segments in result or it is corrupted [#392](https://github.com/hastic/hastic-server/issues/392)
- Wrong time in threshold segments [#403](https://github.com/hastic/hastic-server/issues/403)
- Webhooks don't find any patterns [#401](https://github.com/hastic/hastic-server/issues/401)

#### Changed
- Default config options for docker-compose without .env [#372](https://github.com/hastic/hastic-server/issues/372)
- Log all analytic errors [#353](https://github.com/hastic/hastic-server/issues/353)
- Threshold detector memory [#340](https://github.com/hastic/hastic-server/issues/340)

### [0.2.7-alpha] - 2019-01-22

#### Added
- ElasticSearch support [grafana-datasource-kit/#4](https://github.com/CorpGlory/grafana-datasource-kit/issues/4)
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