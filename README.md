 
# Long Term Support for Node.js Modules
[![Module LTS Adopted'](https://img.shields.io/badge/Module%20LTS-Adopted-brightgreen.svg?style=flat)](http://github.com/CloudNativeJS/ModuleLTS) 

The Long Term Support (LTS) policy for Node.js modules aims to provide the longevity and stability of modules that is crucial for many businesses when adopting Node.js in an enterprise, cloud-native setting.

When a version of Node.js enters LTS, whichever is the latest major version (**X**.y.z) of an LTS adopting module at that time will be supported for at least security and critical fixes for the lifetime of that version of Node.js.

## What does this mean?
Anyone creating an application using an LTS version of Node.js and using the latest major version of LTS adopting modules will will not have to accept semver-major level (ie. breaking) changes into that application in order to receive essential fixes.

Essential fixes are those which will prevent severe issues such as data corruption, and/or pervasive problems likely encountered by any application.

### Worked example

| Module Version | Module Version GA | Minimum EOL | Node Version | Node Version LTS start | Node Version EOL |
|----------------|-------------------|-------------|--------------|------------------------|------------------|
| 2.x.x	        | Sep 2017          | Dec 2019    | Node 8       | Oct 2017               | Dec 2019         |
| 1.x.x	        | Nov 2015          |	Apr 2019    | Node 6       | Oct 2016               | Apr 2019         |
| 1.x.x	        | Nov 2015          |	Apr 2018    | Node 4       | Oct 2015               | Apr 2018         |


In this example, V1 of our module is released in November 2015. Node V4 entered LTS in October 2015, with an End of Life date in April 2018. This means that V1 of our module must remain supported until April 2018 as well.

Node V6 is then released and enters LTS in October 2016.  There have been no breaking API changes delivered to our module and therefore it is still the latest major version. This means it’s End of Life date needs to be extended to Node 6’s End of Life date - April 2019. 

By the time Node V8 reaches LTS in October 2017, we have released V2 of our module. This means that V1 will retain the End of Life date with Node V6 - April 2019, and V2 will be need to be supported for at least the lifetime of Node V8 - until December 2019.

*Note, there is the possibility that a module could be incompatible with the latest version of Node. In this case, the module should be updated. If breaking changes are required this would consistute a new major version of the module, and this new version would have the same End of Life date as the latest version of Node.*


## Additional requirements on modules
* A module must be following semantic versioning (SemVer). Which follows a vX.Y.Z format, where:
  * **X** is a major version change whereby breaking changes are introduced into APIs
  * **Y** is a minor version change where functionality is added in a backwards compatible way
  * **Z** is a patch version change where bug fixes are delivered in a backwards compatible way
* A module must be at least v1.0.0. Within SemVer, before a module reaches V1.x, breaking changes may be introduced into **minor** version changes - and there is an expectation that this module is likely to change frequently.


## Adding LTS to your module

1. Add a badge to your to the `README.md` in your project:

  **Markdown:**
  ```
  [![Module LTS Adopted'](https://img.shields.io/badge/Module%20LTS-Adopted-brightgreen.svg?style=flat)](http://github.com/CloudNativeJS/ModuleLTS)
  ```

  **HTML:**
  ```
  <a href='http://github.com/CloudNativeJS/ModuleLTS'><img src='https://img.shields.io/badge/Module%20LTS-Adopted-brightgreen.svg?style=flat' alt='Module LTS Adopted' /></a> 
  ```

2. Add the following to the `README.md` of your project, modified for the LTS timeline of your modules releases:

  ### Module Long Term Support Policy
  This module adopts the [Module Long Term Support (LTS)](http://github.com/CloudNativeJS/ModuleLTS) policy, with the following End Of Life (EOL) dates:

  | Module Version   | Release Date | Minimum EOL | EOL With     | Status  |
  |------------------|--------------|-------------|--------------|---------|
  | 3.x.x	        | Sep 2017     | Dec 2019    |              | Current |
  | 2.x.x	        | Nov 2015     | Apr 2019    | Node 6       | LTS     |
  | 1.x.x	        | Nov 2015	   | Apr 2018    | Node 4       | EOL     |

3. Raise a Pull Request against this project to have your module added to the Adopters of Module LTS list.

## Adopters of Module LTS

The following Node.js Modules are known to have adopted the Module LTS policy:

| Module                | Type         | LTS Policy        |
|-----------------------|--------------|-------------------|
| [LoopBack](https://www.npmjs.com/package/loopback)              | Framework    | [link](https://github.com/Strongloop/loopback/blob/master/README.md#module-long-term-support-policy)        |
| [cloud-health](https://www.npmjs.com/package/@cloudnative/health)          | Health Check | [link](https://github.com/CloudNativeJS/cloud-health/blob/master/README.md#module-long-term-support-policy) | 
| [cloud-health-connect](https://www.npmjs.com/package/@cloudnative/health)  | Health Check | [link](https://github.com/CloudNativeJS/cloud-health-connect/blob/master/README.md#module-long-term-support-policy) | 
| [appmetrics](https://www.npmjs.com/package/appmetrics)            | Monitoring   | [link](https://github.com/RuntimeTools/appmetrics/blob/master/README.md#module-long-term-support-policy)                  | 
| [appmetrics-dash](https://www.npmjs.com/package/appmetrics-dash)       | Monitoring   | [link](https://github.com/RuntimeTools/appmetrics-dash/blob/master/README.md#module-long-term-support-policy) | 
| [appmetrics-prometheus](https://www.npmjs.com/package/appmetrics-prometheus) | Monitoring   | [link](https://github.com/CloudNativeJS/appmetrics-prometheus/blob/master/README.md#module-long-term-support-policy) | 
| [appmetrics-zipkin](https://www.npmjs.com/package/appmetrics-zipkin)     | Monitoring   | [link](https://github.com/CloudNativeJS/appmetrics-zipkin/blob/master/README.md#module-long-term-support-policy) | 
| [zosconnect-node](https://www.npmjs.com/package/zosconnect-node)       | Connectivity | [link](https://github.com/zosconnect/zosconnect-node/blob/master/README.md#module-long-term-support-policy) | 

