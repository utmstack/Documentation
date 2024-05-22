---
layout: default
title: Integrations
---

<style>
.column-no {
    width: 50px;
}
</style>

# UTMStack Integrations

UTMStack comes out of the box with a wide range of built-in integrations for most mainstream technologies.
Enabling an integration allows UTMStack to correlate logs coming from the corresponding data source on your network and detecting threats reliably.
Each specific integration has its own guide.
Our team is always working on a new integration, but here is the list of what we have developed so far:

*** Integration Requirements *** : To ensure optimal system performance, certain additional requirements beyond the minimums must be considered. Each integration being introduced should reserve at least 1GB of space. This reservation is crucial to ensure proper data storage and efficient system operation as a whole.

*** Logging Volume Considerations ***: Furthermore, it's important to take into account the volume of logs generated and processed within 10-minute intervals. If this volume exceeds 1GB within any time interval, immediate communication with the support team is required. This communication is essential to ensure system stability and performance, as well as to address any potential issues related to log management.


| No. | Name                          |                                                                                                                                  |
| :-: | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------: |
|  1  | VMWare Syslog                 |                          <img title="VMWare" alt="VMWare" src="../Images/Integrations/logovmware.svg">                           |
|  2  | Windows Agent                 |                <img title="Windows Agent" alt="Windows Agent" src="../Images/Integrations/logowindowsagent.svg">                 |
|  3  | Syslog                        |                          <img title="SysLog" alt="Syslog" src="../Images/Integrations/logosyslog.svg">                           |
|  4  | Linux Agent                   |                   <img title="Linux Agent" alt="Linux Agent" src="../Images/Integrations/logolinuxagent.svg">                    |
|  5  | SOC AI                        |                           <img title="SOC AI" alt="SOC AI" src="../Images/Integrations/logosocai.svg">                           |
|  6  | ESET Endpoint Protection      |     <img title="ESET Endpoint Protection" alt="ESET Endpoint Protection" src="../Images/Integrations/logoesetendpoint.svg">      |
|  7  | Kaspersky Security            |         <img title="Kaspersky Security" alt="Kaspersky Security" src="../Images/Integrations/logokasperskysecurity.svg">         |
|  8  | Bitdefender                   |                   <img title="Bitdefender" alt="Bitdefender" src="../Images/Integrations/logobitdefender.svg">                   |
|  9  | Traefik                       |                         <img title="Traefik" alt="Traefik" src="../Images/Integrations/logotraefik.svg">                         |
| 10  | Google Cloud Platform         |         <img title="Google Cloud Platform" alt="Google Cloud Platform" src="../Images/Integrations/logogooglecloud.svg">         |
| 11  | AWS Cloudwatch                |                 <img title="AWS Cloudwatch" alt="AWS Cloudwatch" src="../Images/Integrations/logoawscloud.svg">                  |
| 12  | Office365                     |                      <img title="Office365" alt="Office365" src="../Images/Integrations/logooffice365.svg">                      |
| 13  | Azure                         |                            <img title="Azure" alt="Azure" src="../Images/Integrations/logoazure.svg">                            |
| 14  | Logstash                      |                       <img title="Logstash" alt="Logstash" src="../Images/Integrations/logologstash.svg">                        |
| 15  | MongoDB                       |                         <img title="MongoDB" alt="MongoDB" src="../Images/Integrations/logomongodb.svg">                         |
| 16  | MySQL                         |                            <img title="MySQL" alt="MySQL" src="../Images/Integrations/logomysql.svg">                            |
| 17  | Redis                         |                            <img title="Redis" alt="Redis" src="../Images/Integrations/logoredis.svg">                            |
| 18  | Kafka                         |                            <img title="Kafka" alt="Kafka" src="../Images/Integrations/logokafka.svg">                            |
| 19  | Elasticsearch                 |                <img title="Elasticsearch" alt="Elasticsearch" src="../Images/Integrations/logoelasticsearch.svg">                |
| 20  | PostgreSQL                    |                    <img title="PostgreSQL" alt="PostgreSQL" src="../Images/Integrations/logopostgresql.svg">                     |
| 21  | Kibana                        |                          <img title="Kibana" alt="Kibana" src="../Images/Integrations/logokibana.svg">                           |
| 22  | Cisco Switch                  |                     <img title="Cisco Switch" alt="Cisco Switch" src="../Images/Integrations/logocisco.svg">                     |
| 23  | Cisco ASA                     |                        <img title="Cisco ASA" alt="Cisco ASA" src="../Images/Integrations/logocisco.svg">                        |
| 24  | Cisco Meraki                  |                  <img title="Cisco Meraki" alt="Cisco Meraki" src="../Images/Integrations/logociscomeraki.svg">                  |
| 25  | FortiGate                     |                      <img title="FortiGate" alt="FortiGate" src="../Images/Integrations/logofortigate.svg">                      |
| 26  | Sophos XG                     |                       <img title="Sophos XG" alt="Sophos XG" src="../Images/Integrations/logosophos.svg">                        |
| 27  | Fire Power                    |                     <img title="Fire Power" alt="Fire Power" src="../Images/Integrations/logofirepower.svg">                     |
| 28  | MikroTik                      |                       <img title="MikroTik" alt="MikroTik" src="../Images/Integrations/logomikrotik.svg">                        |
| 29  | Palo Alto                     |                      <img title="Palo Alto" alt="Palo Alto" src="../Images/Integrations/logopaloalto.svg">                       |
| 30  | SonicWall                     |                      <img title="SonicWall" alt="SonicWall" src="../Images/Integrations/logosonicwall.svg">                      |
| 31  | GitHub                        |                          <img title="GitHub" alt="GitHub" src="../Images/Integrations/logogithub.svg">                           |
| 32  | Nats                          |                             <img title="Nats" alt="Nats" src="../Images/Integrations/logonats.svg">                              |
| 33  | Json Input                    |                       <img title="Json Input" alt="Json Input" src="../Images/Integrations/logojson.svg">                        |
| 34  | MacOS                         |                            <img title="MacOS" alt="MacOS" src="../Images/Integrations/logomacos.svg">                            |
| 35  | OsQuery                       |                         <img title="OsQuery" alt="OsQuery" src="../Images/Integrations/logoosquery.svg">                         |
| 36  | Linux Auditing Demon          |         <img title="Linux Auditing Demon" alt="Linux Auditing Demon" src="../Images/Integrations/logolinuxauditing.svg">         |
| 37  | Deceptive Bytes               |             <img title="Deceptive Bytes" alt="Deceptive Bytes" src="../Images/Integrations/logodeceptivebytes.svg">              |
| 38  | High Availability Proxy       |        <img title="High Availability Proxy" alt="High Availability Proxy" src="../Images/Integrations/logohighproxy.svg">        |
| 39  | File Classification           |       <img title="File Classification" alt="File Classification" src="../Images/Integrations/logofileclassification.svg">        |
| 40  | Apache                        |                          <img title="Apache" alt="Apache" src="../Images/Integrations/logoapache2.svg">                          |
| 41  | Internet Information Services |     <img title="Internet Information Services" alt="Internet Information Services" src="../Images/Integrations/logoiis.svg">     |
| 42  | Nginx                         |                            <img title="Nginx" alt="Nginx" src="../Images/Integrations/logonginx.svg">                            |
| 43  | Sophos Central                |               <img title="Sophos Central" alt="Sophos Central" src="../Images/Integrations/logosophoscentral.svg">               |
| 44  | SentinelOne Endpoint Security | <img title="SentinelOne Endpoint Security" alt="SentinelOne Endpoint Security" src="../Images/Integrations/logosentinelone.svg"> |
| 45  | PfSense                       | <img title="SentinelOne Endpoint Security" alt="SentinelOne Endpoint Security" src="../Images/Integrations/pfsenselogo.png" width="200" height="200">     |
| 46  | IBM AIX                       | <img title="SentinelOne Endpoint Security" alt="SentinelOne Endpoint Security" src="../Images/Integrations/IBMAIXlogo.png" width="200" height="200">  |
| 47  | FortiWeb                      | <img title="SentinelOne Endpoint Security" alt="SentinelOne Endpoint Security" src="../Images/Integrations/logofortigate.svg">   |
| 48  | NetFlow                       | <img title="SentinelOne Endpoint Security" alt="SentinelOne Endpoint Security" src="../Images/Integrations/netflowlogo.png" width="100" height="100">     |



