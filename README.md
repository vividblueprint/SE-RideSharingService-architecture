![Adove Ride Logo](https://github.com/adobe/ride/raw/develop/images/RideLogo.jpg)
<h3 align="center">Ride Sharing Service</h3>

<div align="center">

  [![Tweet](https://img.shields.io/twitter/url/https/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=%F0%9F%93%A2%20Various%20README%20templates%20and%20tips%20on%20writing%20high-quality%20documentation%20that%20people%20want%20to%20read.&url=https://github.com/kylelobo/The-Documentation-Compendium)
  [![Status](https://img.shields.io/badge/status-active-success.svg)]()
  [![GitHub Issues](https://img.shields.io/github/issues/kylelobo/The-Documentation-Compendium.svg)](https://github.com/kylelobo/The-Documentation-Compendium/issues)
  [![GitHub Pull Requests](https://img.shields.io/github/issues-pr/kylelobo/The-Documentation-Compendium.svg)](https://github.com/kylelobo/The-Documentation-Compendium/pulls)
  [![License](https://img.shields.io/badge/license-CC0-blue.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

  <a href="https://www.producthunt.com/posts/the-documentation-compendium?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-the-documentation-compendium" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=157965&theme=dark&period=daily" alt="The Documentation Compendium - Beautiful README templates that people want to read. | Product Hunt Embed" style="width: 250px; height: 54px;" width="250px" height="54px" /></a>

</div>

---

<p align = "center">💡 Various templates & tips on writing high-quality documentation that people want to read.</p>


## Table of Contents

* [Project description](#project-description)
* [Business goals](#business-goals)
* [Stackholders](#stackholders)
* [Functional Requirements](#functional-requirements)
* [Quality Attribute](#quality-attribute)
  - [Consistency](#consistency)
  - [Availability](#availability)
  - [Scalability](#scalability)
  - [Flexibility](#flexibility)
  - [Security](#security)
  - [Performance](#performance)
* [Viewpoint](#viewpoint)

## Project description

When it comes to getting about in cities, many people choose ride-sharing apps like Uber or Lyft. Indeed, such apps make short-range commute very easy by offering competitive pricing, reasonably short wait time, high security and high availability. From a technical point of view, systems like these are very interesting because nearest-neighbor searching is hard. These systems have much more complex architecture and there are a lot of components joined together internally to provide riding services all over the world. 
A user can request a ride through the application and within a few minutes, a driver arrives nearby his/her location to take them to their destination. It has a backend service, a frontend service, and a single database.

## Business goals

  <li> To achieve 99.99% reliability of the core travel experience on ride sharing service (only have a total of one hour of downtime per year, and a maximum of one minute per week, in other words, every 10,000 operations can only fail 1 time at a time.</li>
  <li>Codebase divided by 2: Core code, and optional code. Core code is compulsory when the rider register, calls and completes or cancels travel requirements. Any modification to the core code must go through a rigorous review process. Optional code is less reviewed and can be dynamically closed at any time. This encourages mutual independence at the code level, allowing us to try new features and stop them at any time.</li>
  <li>Core architecture: class names, inheritance relationships between business logic units (inheritance relationship between business logic units), main business logic, plugin point (name, dependency, structure, etc.), reactive programming chains (relationship between reactive programming), unified platform components (unified platform-level modules).</li>
</ol>

## Stackholders

The main stakeholders and users of the ride sharing service are the admin (ride sharing company), Passengers and Drivers. 

## Functional Requirements

- Riders can view nearby drivers
- Riders can request a ride
- Riders can view the driver’s ETA and approximate price
- Driver accepts the trip; the rider can view the driver’s location and communicate until trip completion.
- Book a cab
- Match riders with drivers
- See cabs in your vicinity
- Location tracking
- Post-tractions: Collect ratings, send emails, update databases, schedule payments
- Price and Surge: the price is increased when there are more demand and less supply with the help of prediction algorithms. According the ride-sharing service helps to meet supply demands by increasing the price, more cabs will be on the road when the demand is more.

## Quality Attribute

### Consistency
Mission-critical applications such as financial dashboards require data to be consistent across all regions. This includes zero data loss in the inter-region and intraregional dispersal and processing mechanisms, de-duplication as well as ability to certify data quality.

### Availability
The real time data infrastructure stack must be highly available with 99.99 percentile guarantee. Loss of availability has a direct impact on ride sharing business and may result in significant financial losses. For instance, dynamic pricing leverages the real-time data infrastructure component for calculating demand and supply ratios per geo-fence, which in turn is used to influence the price of a trip.

### Scalability
The raw data streams constitute petabytes of data volume collected per day across all regions. This data is constantly growing based on organic growth of our user base, new lines of business deployed by ride sharing company as well as new real time analytics use cases that arise over time. The ability to scale with this ever-growing data set in a seamless manner, without requiring users to re-architect the processing pipelines is a fundamental requirement of the real-time data infrastructure stack.

### Flexibility
We need to provide programmatic as well as declarative (SQL like) interface for expressing computational logic to accommodate the diverse user groups. In addition, some use cases need a push-based model which is semi stateful and continuously emits generated results whereas others might need a stateful pull-based model where the user can execute queries on the raw data stream. For instance, users can create intelligent alerts in case of business rule violation using push-based stream processing pipelines. Whereas, dashboarding and triaging will require a pull-based SQL interface for the same datasets.

### Security
This system has multistep security. The user needs to login to the system every time by providing a password and user ID, and the login session will time out after every 2 minutes to ensure high security. When the passenger pays the bill, they need to again give the password. All of those steps will keep their bank card and payment information secure. In bellow see full description about security.

Basic security behaviors:
- Authentication: Login using at least a user name and a password
- Authorization: according to their profile, online user must be granted or not allowed to receive some specific services (Automatic match finding, Ride Suggestion, etc...)
For internet access, the following requirements are mandatory
- Confidentiality: sensitive data must be encrypted if any (credit card payments).
- Safety: Credit card data must not be kept at a local database.
- Data integrity: Data sent across the network cannot be modified by a tier
- Auditing: Every sensitive action can be logged
- Non-repudiation: gives evidence a specific action occurred

### Performance
This system has high performance ability. Passengers can book a taxi and search for availability in a short period of time. Admin can update the bike taxi list. Search queries should return 90% of the time below 5 seconds. The credit card payment transaction should finish in 10 seconds.

## Viewpoint

The system has some viewpoint. 

- Use-Case view
- Logical view
- Development view
