# Cribl Pack for AWS CloudTrail Data Collection 
----

This pack will help collect your Amazon Web Services (AWS) CloudTrail logs from an existing S3 bucket and into your logging solution of choice. The pipelines will help remove unnecessary fields and events thus reducing the noise and clutter of CloudTrail events. This pack is based on the blog post https://cribl.io/blog/threat-hunting-while-staying-compliant-categorizing-and-scoring-aws-cloudtrail-events-in-real-time/ . From here we built a content pack that helps lay the groundwork for collecting CloudTrail logs.

## Uses for Cribl Content Pack
----
- Share CloudTrail data between accounts / teams with the peace of mind that sensitive data is being redacted.
- Easily consume AWS CloudTrail data without having to ingest useless fields and events. Lower the cost of collecting these chatty logs.
- Test out new security products by simply adding a new route to send your data. 
- Replay old CloudTrail logs into ML/AI based security products to see if are any unknown threats or issues in your environment.

## Requirements Section

Before you begin, ensure that you have met the following requirements:

* Access to your CloudTrail S3 Bucket
* A working Cribl LogStream Cloud Account

## Release Notes

### Version 0.0.1 - 2022-01-05
In this release, we have a couple simple use cases for CloudTrail data. 

## Contributing to the Pack
To contribute to the Pack, please do the following:
 - Pipelines :
    - To mask / redact sensetive data such as Account ID's, Access / Secret Keys
    - Remove cypher keys from events
    - Drop Describe, List and Get events
    - Lookup IP Addresses against a known list of AWS sourced IP ranges
- Knowledge 
    - Added list of AWS IP's from https://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html 
    - Custom Regex for Amazon Web Services Account ID

Feel free to update the github for this pack : https://github.com/criblpacks/cribl-aws-cloudtrail-logs 

## Contact
Kam Amir - Cribl : [`kam@cribl.io`](mailto:kam@cribl.io?Subject="Cribl%20CloudTrail%20Content%20Pack")

## License
This Pack uses the following license: [`Apache 2.0 `](https://www.apache.org/licenses/LICENSE-2.0)