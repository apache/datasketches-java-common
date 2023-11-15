<!--
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
-->

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.datasketches/datasketches-java-common/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.apache.datasketches/datasketches-java-common)
[![Language grade: Java](https://img.shields.io/lgtm/grade/java/g/apache/datasketches-java-common.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/apache/datasketches-java-common/context:java)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/apache/datasketches-java-common.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/apache/datasketches-java-common/alerts/)
[![Coverage Status](https://coveralls.io/repos/github/apache/datasketches-java-common/badge.svg)](https://coveralls.io/github/apache/datasketches-java-common?branch-main)

=================

# Apache<sup>&reg;</sup> DataSketches<sup>&reg;</sup> Java Common Test Component
This artifact contains common java classes and methods to support test code in multiple different Java repositories.  

The code in this artifact is not tested as rigorously or documented as thoroughly as main runtime code. Caveat Emptor!

This artifact may be included as a test scope dependency, but never included as a dependency for main runtime code.

Please visit the main [DataSketches website](https://datasketches.apache.org) for more information about the Apache DataSketches project. 

If you are interested in making contributions to this site please see our [Community](https://datasketches.apache.org/docs/Community/) page for how to contact us.

## Maven Build Instructions
__NOTE:__ This artifact may include resource files for testing. As a result, the directory elements of the full absolute path of the target installation directory must qualify as Java identifiers. In other words, the directory elements must not have any space characters (or non-Java identifier characters) in any of the path elements. This is required by the Oracle Java Specification in order to ensure location-independent access to resources: [See Oracle Location-Independent Access to Resources](https://docs.oracle.com/javase/8/docs/technotes/guides/lang/resources.html)

### A JDK-8 with Hotspot or JDK-11 with Hotspot is required to compile

### This artifact depends on TestNG.
The TestNG version must support JDK-8. And if your environment is JDK-9 or higher a different TestNG version may be required.

### Recommended Build Tool
This DataSketches component is structured as a Maven project and Maven is the recommended Build Tool.

There are two types of tests: normal unit tests and tests run by the strict profile.  

To run normal unit tests:

    $ mvn clean test

To run the strict profile tests (only supported in Java 8):

    $ mvn clean test -P strict

To install jars built from the downloaded source:

    $ mvn clean install -DskipTests=true

### Dependencies

#### Run-time
There are no run-time dependencies

#### Testing
See the pom.xml file for test dependencies.

## Known Issues

#### SpotBugs

* Make sure you configure SpotBugs with the /tools/FindBugsExcludeFilter.xml file. Otherwise, you may get a lot of false positive or low risk issues that we have examined and eliminated with this exclusion file.
