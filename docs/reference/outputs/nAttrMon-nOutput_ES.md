---
layout: default
title: ES
parent: Outputs
grand_parent: Reference
---

_tbc_

Examples:

````yaml
output:
  name         : Output ES values
  chSubscribe  : nattrmon::cvals
  waitForFinish: true
  onlyOnEvent  : true
  execFrom     : nOutput_ES
  execArgs     :
    url      : http://127.0.0.1:9200
    #user     : nouser
    #pass     : nopass
    #index: 
    #considerSetAll: false 
    #funcIndex: "ow.ch.utils.getElasticIndex('nattrmon-attrs',\"yyyy.ww\")" note: Check getElasticIndex function, If a specific format is needed you can provide it as aFormat (see ow.format.fromDate)"
    funcIndex: "ow.ch.utils.getElasticIndex('nattrmon-attrs')"
    #index: nattrs
    stampMap :
      region: US
    #include  :
    #  - test/test 1
    # exclude  :
````

````yaml
output:
  name         : Output ES warnings
  chSubscribe  : nattrmon::warnings
  waitForFinish: true
  onlyOnEvent  : true
  execFrom     : nOutput_ES
  execArgs     :
    url      : http://127.0.0.1:9200
    #user     : nouser
    #pass     : nopass
    #index: 
    #considerSetAll: false 
    #funcIndex: "ow.ch.utils.getElasticIndex('nattrmon-attrs',\"yyyy.ww\")" note: Check getElasticIndex function, If a specific format is needed you can provide it as aFormat (see ow.format.fromDate)"
    funcIndex: "ow.ch.utils.getElasticIndex('nattrmon-warns')"
    #index: nattrs
    stampMap :
      region: US
    #include  :
    #  - test/test 1
    # exclude  :
````