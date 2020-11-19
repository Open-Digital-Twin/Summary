# Open-Digital-Twin Summary
Repository for documenting the different repositories associated with the Open-Digital-Twin group.

## Repository Organization

For hosting the project codebase and testing scripts, the "Open Digital Twin" organization was created on GitHub.
The architecture is an open-source software built as a collection of individual microservices, available under the GNU General Public License v3.0. Currently, the organization hosts 11 repositories related to this project. In the following sections, the different repository types and individual repositories will be described and related.

### Architecture repositories

Repositories which names start with "dt" are implementations of the Digital Twin architecture. 

* *[dt-client](https://github.com/Open-Digital-Twin/dt-client)* and *[dt-client-bytes](https://github.com/Open-Digital-Twin/dt-client-bytes)*: Testing repositories to simulate data acquisition via publishing to an MQTT broker, allowing for customization of the number of messages published, its frequency, and payload. They represent the "real" aspect of the system and act as elements with data sources. The repositories act as the emulated devices, communicating with the DT instance using the *[rumqttc](https://github.com/bytebeamio/rumqtt)* MQTT client;

* *[dt-instance](https://github.com/Open-Digital-Twin/dt-instance)* and *[dt-instance-webserver](https://github.com/Open-Digital-Twin/dt-instance-webserver)*: instance of the created Digital Twins. The *dt-instance* includes communication with the message broker and storage of acquired data, while *dt-instance-webserver* is an optional service containing a Representational State Transfer (REST) Application Programming Interface (API) for configuring the instance elements, data sources, and other configuration related to the DT instance. The DT instance is a prototype of the digital aspect of the system, providing means for acquisition, storage, and processing of data, and is where the physical product is linked throughout its entire lifecycle. The DT instance is the final destination for the client messages, after being distributed by the broker. They represent the "digital" aspect of the system;
* *[dt-master](https://github.com/Open-Digital-Twin/dt-master)*: Central Digital Twin microservice, where users can create and deploy new DT instances;
* *[dt-common](https://github.com/Open-Digital-Twin/dt-common)*: Shared modules used in multiple projects, to be used as a Git submodule, for reuse of DT-related code between the components;
* *[dt-sharedconfig](https://github.com/Open-Digital-Twin/dt-sharedconfig)*: Shared configuration used in multiple projects, like database initialization.

### Article testing repositories

Repositories which names start with "article-test" are code used directly in testing for the case studies presented by this work. These include scripts for exporting and parsing raw data for analysis shown in studies with the twin framework.

* *[article-test-fog](https://github.com/Open-Digital-Twin/article-test-fog)*: Scripts used for testing in the cloud and fog deployment scenarios of the architecture.
* *[article-test-mqtt-sender](https://github.com/Open-Digital-Twin/article-test-mqtt-sender)* and *[article-test-mqtt-receiver](https://github.com/Open-Digital-Twin/article-test-mqtt-receiver)*: Scripts used for tests which studies the usage of the MQTT protocol for Digital Twins.

### General repositories

Repositories that do not have a specific category, but are relevant to the project and the organization.

* *[Summary](https://github.com/Open-Digital-Twin/Summary)*: You are here. Meta repository, for documenting the organization. Repository for documenting the different repositories associated with the Open-Digital-Twin group projects.


