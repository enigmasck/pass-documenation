# Journal

A Journal is associated with a [Publication](Publication.md). In some cases, the Journal may be important for determining whether the [User](User.md) needs to manually create a [Submission](Submission.md) through PASS or whether the publisher has a pre-existing arrangement with the target [Repository](Repository.md). Specifically, in the case of the National Institutes of Health Public Access Policy, many Journals already make arrangements to submit the author's accepted manuscript to PubMed Central directly.

| Field         | Type          | Description |
| ------------- | ------------- | ------------- |
| id* | String | Autogenerated identifier of object |
| journalName* | String | Name of the journal |
| issns | String[] | Journal ISSNs - Elements are of the form type:value, where type is one of Online or Print, and value is the usual ISSN value xxxx-xxxx. Examples would be Online:1234-5678 and Print:9876-5432. When a type for an ISSN is not known, it should be stored with an empty type (for example :2468-1357).|
| nlmta | String | National Library of Medicine Title Abbreviation |
| pmcParticipation | String | This field indicates whether a journal participates in the NIH Public Access Program by sending final published article to PMC. If so, whether it requires additional processing fee ([see list below](#pmc-participation-options)) |

*required 

## PMC Participation options

These are the possible submission methods relating to PMC deposits. A full description of these methods can be found on the [NIH public access website](https://publicaccess.nih.gov/submit_process.htm)

| Value         | Description |
| ------------- | ------------- | 
| A | PMC deposit route A. Journals automatically post the paper to PMC |
| B | PMC deposit route B. Authors must make special arrangements for some journals and publishers to post the paper directly to PMC |
| C | PMC deposit route C. Authors or their designee must submit manuscripts to NIHMS |
| D | PMC deposit route D. Some publishers will submit manuscripts to NIHMS |