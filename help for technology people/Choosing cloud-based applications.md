##Choosing cloud-based applications

Guidance for government departments wanting to adopt cloud applications in line with the cloud first policy.

The [Technology Code of Practice](https://www.gov.uk/government/publications/technology-code-of-practice/technology-code-of-practice) asks you to adopt cloud first, to evaluate public cloud services first, and to only choose other kinds of application where you can prove they offer better value for money for comparable functionality.
###Choose genuine public cloud applications

It can be difficult to know when and application is genuine cloud and not a hosted application rebadged as ‘cloud’, or some sort of hybrid arrangement.  We prefer genuine public cloud applications in most cases.  They can operate at greater scale, as a result tend to offer more innovation, reliability, and lower cost, but can carry [greater risk](https://www.ncsc.gov.uk/guidance/separation-and-cloud-security#publicC). Public cloud applications should:

* be multi-tenanted, serving multiple customers from shared infrastructure
* provide consistent availability and performance irrespective of demand
* device agnostic and usually browser and mobile first
* use a subscription licensing model
* use virtualised infrastructure and scale invisibly to the user
* provide regular updates without service disruption
* let you sign up for a free trial without the vendor’s help
* provide open APIs

You may also come across two other types of cloud service:

* community, where a group, like the public sector, shares infrastructure
* private, where only a single organisation can use the service

Community cloud applications provide additional security benefits at the cost of scalability, reliability, flexibility and innovation. Private cloud goes a step further to restrict to a single organisation.  While these may be appropriate in some circumstances they are likely to be a rebadged traditional hosting arrangement rather than a genuine cloud service, and do not meet the [cloud first policy](https://www.gov.uk/government/news/government-adopts-cloud-first-policy-for-public-sector-it).

Be wary of ‘cloudwashing’ where organisations build or repackage existing applications that might fit some of the definition of cloud (like providing APIs) but don’t provide the benefits like elasticity and frequent updates of real cloud applications.

Hints that an application might not be a genuine [multi-tier](https://en.wikipedia.org/wiki/Multitier_architecture) cloud service are outages for updates, or the capability for some customers to remain on older versions, the ability to host private instances, including on-premise

###Understand and meet user needs

Replacing legacy applications with cloud-based alternatives can often mean changing internal processes and training end users.

Existing processes may have been built around the way systems worked at the time (for example, limited storage space).  Research and understand the needs you are trying to meet and buy the cloud-based applications that best meet those needs.  Don’t try to meet needs that haven’t been expressed or are not self-evident

###Consider how best to provide applications
You may not want to replace an existing application like for like. User needs may have changed since a legacy application was introduced, or different technologies may be able to meet the needs in a different but better way. It may also be more sensible to use several smaller applications rather than a single application suite.  For example if you currently do absence management in your [enterprise resource planning software (ERP)](https://en.wikipedia.org/wiki/Enterprise_resource_planning) you may find it better to use a separate cloud-based absence management application that sends information back to your existing ERP, rather than replace the entire ERP in one go.

###Limit bespoke configuration, couple services loosely, and plan to leave

You should be able to swap out applications easily and cheaply when you change your mind or as understanding of how to meet user needs changes. Limit customisations to prevent getting locked into a particular solution.

You should be able to export data and configuration in standard, reusable formats to allow you to move to a new supplier if you want to.  Consider the cost of this as part of buying the application, not the cost of its replacement, otherwise you may find yourself technically able to move but locked in financially. 

###Share between applications rather than sharing applications

Organisations in government can change shape and purpose, and technology will always develop. Organisations should retain their autonomy to manage their own costs, operate at their own risk appetite, and makes changes at their own pace.  Entering into a larger shared environment for something like email and productivity can make sense initially but adds risk of expensive data migrations when organisations change, and can force you to make choices that don’t best meet your user needs.

In most cases you can either share information between tenancies in the same application, or give access to your own tenancy to those who need it in other organisations.

###Security

NCSC provide a [range of guidance](https://www.ncsc.gov.uk/index/guidance?f[0]=field_topics%253Aname%3ACloud%20security) on security in cloud-based applications. You should evaluate applications using the Cloud Security Principles and make decisions based on your organisation’s risk appetite and data.

###Continue to manage your information

Make sure you know how your users will be able to keep important work information for the permanent record and know how to do it.  This could mean copying or exporting data in a reusable format into a system of record, applying information management policy within the application, or using a third party service or plugin to provide the functions you need.

###Support

Support can work differently for cloud-based applications compared to legacy on-premise applications.  Problems that affect your organisation are likely to affect many other organisations at the same time, particularly if you are using a public cloud application.  Service credits are unlikely to affect reliability or provide sufficient compensation so a proven record or 99.99%+ reliability is important.  Talk to existing customers and study past performance. Status dashboard and feeds should be public.

In some cases the overall application may work but smaller aspects of it might not, so consider the real effect on users. Problems should be spotted more quickly, particularly for more popular public cloud services, so may be fixed before your users notice.

###Test the service

Never buy a service both you and your users haven’t tried. Cloud providers should be able to give you access to most services with little to no effort or configuration.
