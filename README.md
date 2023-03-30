<br>
<br><p align=center><img width=400 src="https://jugnoo.io/wp-content/uploads/2021/05/2-1024x536.png"/></p>

<h1 align="center" >
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/>
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/>
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/>
<b>Ride Sharing Service</b>
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/>
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/>
<img width=25px src="https://em-content.zobj.net/source/microsoft-teams/337/heart-with-ribbon_1f49d.png"/></h1>
 <p align="center">Get dynamically generated GitHub stats!</p>

<p align="center">
  <a href="https://github.com/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture/actions">
    <img alt="Tests Passing" src="https://github.com/anuraghazra/github-readme-stats/workflows/Test/badge.svg"/>
  </a>
  <a href="https://github.com/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture/contributors">
    <img alt="GitHub Contributors" src="https://img.shields.io/github/contributors/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture"/>
  </a>
  <a href="https://github.com/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture/issues">
    <img alt="Issues" src="https://img.shields.io/github/issues/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=0088ff"/>
  </a>
  <a href="https://github.com/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture/pulls">
    <img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=0088ff">
  </a>
  <br />
<img alt="Lines of code" src="https://img.shields.io/tokei/lines/github/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=green">
<img alt="GitHub language count" src="https://img.shields.io/github/languages/count/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=302df0">
<img alt="GitHub top language" src="https://img.shields.io/github/languages/top/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture">
<img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=0088ff">
<img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture?color=00ff00f">
<img alt="GitHub repo file count" src="https://img.shields.io/github/directory-file-count/WHU-Ride-Sharing-Service/SE-RideSharingService-architecture">
</p>

---

## Table of Contents

- [Introduction](#introduction)
- [Business Requirements](#business-requirements)
- [Stakeholder Analysis](#stakeholder-analysis)
- [Architecture Principles](#architecture-principles)
- [Architecture Components](#architecture-components)
- [Functional Requirements](#functional-requirements)
- [Viewpoint](#viewpoint)
  - [Functional Viewpoint](#functional-viewpoint)
  - [Development Viewpoint](#development-viewpoint)
  - [Deployment View](#deployment-view)
  - [Context Viewpoint](#context-viewpoint)
- [Quality Attribute](#quality-attribute)
  - [Consistency](#consistency)
  - [Availability](#availability)
  - [Scalability](#scalability)
  - [Flexibility](#flexibility)
  - [Security](#security)
  - [Performance](#performance)
- [Technical Debt](#technical-debt)
- [Conclusion](#conclusion)
- [References](#references)
- [Appendix](#appendix)

# Introduction

The ride-sharing industry has exploded in popularity in recent years, with services such as Uber, Lyft, and Grab becoming ubiquitous in cities around the world. These services offer a new and convenient way for people to get around, using a combination of technology and transportation to connect riders with drivers. However, designing and implementing a successful ride-sharing service is no simple feat, and requires careful consideration of a wide range of technical, logistical, and social factors.

This software architecture document aims to provide a detailed overview of the architecture of a ride-sharing service, including the key components and systems involved in its operation. This document is intended for developers, architects, and stakeholders who are involved in the development or management of a ride-sharing service, and who need to understand the technical aspects of the service in order to make informed decisions.

The document will begin by providing an overview of the ride-sharing industry, including the key players and trends that have emerged in recent years. This will be followed by a detailed description of the architecture of a typical ride-sharing service, including the key components such as the rider app, driver app, and backend systems. The document will also cover topics such as data privacy and security, scalability and performance, and integration with third-party services.


Overall, this document aims to provide a comprehensive and practical guide to the architecture of a ride-sharing service, with a focus on the technical considerations and challenges involved in designing and operating such a service. By providing a clear and detailed understanding of the key systems and components involved in a ride-sharing service, this document will help developers and stakeholders to make informed decisions and build successful ride-sharing services that meet the needs of riders, drivers, and other stakeholders.

# Business Requirements

Before we dive deeper into the architecture of the ride-sharing service, let's first define the business requirements. The ride-sharing service should meet the following requirements:

1. Passenger and Driver Registration: The service should allow passengers and drivers to easily register and create accounts.

1. Ride Requests: Passengers should be able to request rides using the app, specifying their pickup and dropoff locations, and the type of vehicle they want. Drivers should receive notifications of incoming ride requests.

1. Driver Acceptance: Drivers should be able to accept or reject ride requests based on their availability.

1. Navigation: The app should provide navigation instructions to the pickup and dropoff locations for both passengers and drivers.

1. Real-Time Tracking: Passengers should be able to track the driver's location in real-time.

1. Payment Processing: The service should process payments securely and efficiently, handling refunds, chargebacks, and disputes.

1. Ratings and Reviews: Passengers and drivers should be able to rate each other and leave reviews.

1. Customer Support: The service should provide customer support to handle issues and complaints.

1. Reducing costs: Companies aim to optimize their operations to reduce costs, including driver acquisition and retention, maintenance of vehicles, and marketing expenses.

Now that we have defined the business requirements, let's move on to the architecture of the ride-sharing service.

# Stakeholder Analysis
In the case of a ride-sharing service, stakeholders can include a wide range of individuals or groups who have an interest or investment in the success of the service. Some examples of stakeholders in a ride-sharing service might include:

1. Investors: Investors who have put money into the ride-sharing service and expect a return on their investment. These investors may include venture capitalists, angel investors, or institutional investors.

1. Riders: People who use the ride-sharing service to get from one place to another. These individuals have a stake in the success of the service because they rely on it for transportation.

1. Drivers: Individuals who work for the ride-sharing service and provide rides to riders. Drivers have a stake in the success of the service because their livelihood depends on it.

1. Administrators: People who are responsible for managing the ride-sharing service, including making decisions about pricing, marketing, and customer support.

1. Regulators: Government agencies or other entities that have regulatory authority over the ride-sharing service. These regulators may have an interest in ensuring that the service operates in compliance with local laws and regulations.

Competitors: Other companies that offer ride-sharing services and may be impacted by the success of the service.

Each stakeholder group may have different goals, interests, and expectations for the ride-sharing service, and it's important to consider their perspectives when designing the architecture of the service. By understanding the needs and goals of each stakeholder group, architects can design a ride-sharing service that meets the needs of everyone involved and is well-positioned for success.

In addition to the stakeholders who have a positive interest or investment in the success of the ride-sharing service, there may also be negative stakeholders who have concerns or objections to the service. Some examples of negative stakeholders in a ride-sharing service might include:

1. Taxi companies: Traditional taxi companies may see ride-sharing services as competition and may have negative opinions about the service. They may lobby against the service or try to block its entry into certain markets.

1. Local governments: Some local governments may have concerns about the impact of ride-sharing services on traffic congestion, public safety, and revenue from traditional taxi and transportation fees. They may impose regulations or taxes on the service that increase costs or limit its operations.

1. Labor unions: Labor unions may have concerns about the working conditions and wages of ride-sharing service drivers. They may lobby for greater protections or regulations that limit the flexibility or earning potential of drivers.

1. Environmental groups: Environmental groups may be concerned about the impact of ride-sharing services on air quality and carbon emissions. They may advocate for alternative transportation solutions or policies that limit the use of ride-sharing services.

1. Privacy advocates: Privacy advocates may have concerns about the collection and use of user data by ride-sharing services. They may advocate for greater privacy protections or transparency around how user data is collected and used.

Understanding the concerns and objections of negative stakeholders is important in designing a ride-sharing service that is sustainable and responsive to the needs of all stakeholders. By considering the perspectives of both positive and negative stakeholders, architects can design a ride-sharing service that addresses concerns and objections while still meeting the needs of riders, drivers, investors, and other positive stakeholders.


# Architecture Principles
# Architecture Components
# Functional Requirements
## Functional Requirements

### Essential Requirements of Rider/Passenger Interface

- Registration: Riders can register or sign in via email and social media. They can also register for different payment methods.
- Riders can request a ride
- Taxi Booking: The riders can book a taxi, enter their address, select the type of car, and adjust the pickup location. 
- Fare Calculator: The fare for traveling from point A to point B is automatically calculated based on the number of kilometers, the type of car chosen, current fuel rates, estimated traffic, etc
- Ride Tracking: The driver’s location is tracked in Real-time based on which timely updates on traffic, travel routes, and the estimated time of arrival is provided to the rider.
- Payment: Cashless and in-app payment features are at the rider’s disposal. They can choose from various options, including credit cards, debit cards, net banking, PayPal, etc. 
- Messaging & Calling: Messages and calls to the rider providing the status of their ride.
- Driver Rating & Analysis: Provide driver rating based on the journey, taken route, car comfort, driver’s behavior, etc.
- Travel History: The track record of the previous rides and transactions.
- Ride Cancellation: The rider has the option of canceling the ride, but needs to be done within a specified time limit to avoid paying the  cancellation fee.
- Split Payment: Riders also can opt to share a ride with other passengers. 
- Schedule for Later: This feature allows the riders to book a ride in advance. 
- Book for Others: Using this feature, one can also book a taxi for their friends, relatives, colleagues, etc.


### Essential Requirements of Driver Interface

- Driver Profile & Status: This feature gives the complete information of the driver, for example: if he/she is verified or not, their license, car insurance, etc. The driver’s availability status is also displayed through this feature.
- Trip Alert: The driver would be notified for incoming ride requests, information on the destination, pickup location, travel route, and rider’s necessary details.
- Push Notifications: Notifications are received when the ride commences, any change in the travel route, heavy traffic ahead and on the completion of the ride
- Navigation & Route Optimization: The driver uses this feature to navigate the traffic, opt for the shortest way to the destination using the Google Maps
- Reports: Provide insights regarding trips and earnings on a daily/weekly/monthly basis
- Waiting time: The rider would be charged extra if the waiting period exceeds 5minutes.
- Next Ride: The ride is notified of an upcoming ride while he/she is still completing the previous one.


### Essential Requirements of Admin Interface
An Admin panel is crucial for the proper integration and smooth functioning of the system.

The basic features and functionalities of an Admin panel would be:

- Customer and Driver Details Management (CRM)
- Booking Management
- Vehicle Detail Management (if self-owned)
- Location and Fares Management
- Call System Management
- Communication
- Ratings and Reviews
- Promotions and Discounts
- Payroll Management
- Content Management
- Customer Support and Help


# Viewpoint

### Use Case Viewpoint

Ride sharing services have become a popular mode of transportation for people all over the world. They offer an affordable and convenient way to get around, and can be accessed through a variety of platforms, including mobile apps and websites. In this Use Case Viewpoint, we will examine the different use cases for ride sharing services, including how they are used by passengers and drivers.

### Actors:

These actors play a crucial role in the ride sharing service use case. The primary users (Rider, Ride Sharing Company, and Driver) are responsible for the core functionality of the service, while the secondary users (GPS, Navigation Engine, and Payment Gateway) provide supporting functions to ensure that the ride is completed efficiently and securely.

#### Primary users:

1. Rider: A person who needs a ride from one location to another.
1. Driver: A person who provides a ride to a rider using their own vehicle.
1. Ride Sharing Company: The organization that provides the ride sharing service and manages the API.

#### Secondary users:
1. GPS (Global Positioning System): GPS is an actor that is responsible for providing real-time location data to the ride sharing service.
1. Navigation Engine: Navigation Engine is an actor that provides route guidance to the driver during the ride. The use case of Navigation Engine involves providing real-time traffic information, suggesting alternate routes, and providing turn-by-turn directions to the driver.
1. Payment Gateway: Payment Gateway is an actor that facilitates the transaction between the rider and the ride sharing service. The use case of Payment Gateway involves securely processing the payment information, verifying the transaction, and transferring the funds to the ride sharing service.

#### Use Cases:

1. Request a Ride
- Rider opens the ride sharing service app and enters their destination.
- Ride sharing service uses GPS to determine the rider's location and matches the rider with an available driver who is nearby and notifies the driver of the request.
- Driver accepts the ride request and the Navigation Engine provides turn-by-turn directions to navigate to the pick-up location.
1. Start Ride
- Driver picks up the rider at the pick-up location.
- Driver starts the ride in the app to begin tracking the distance and time of the ride using GPS.
- Navigation Engine provides turn-by-turn directions to the destination.
1. End Ride
- Driver completes the ride in the app when they arrive at the destination.
- Rider confirms that the ride has ended and pays for the ride through the app, with GPS being used to calculate the fare based on distance and time.
- GPS is used to track the vehicle's location and calculate the fare.
- Navigation Engine provides the driver with the most efficient route to the destination, which helps to reduce the time and distance of the ride.
1. Cancel Ride
- Rider cancels the ride request before the driver arrives.
- Ride sharing service cancels the ride and notifies the driver, with GPS being used to update the driver's location.
- Navigation Engine provides the driver with updated directions to their next destination.
1. Update Ride Details
- Rider updates the pick-up location or destination of the ride request before the driver arrives.
- Ride sharing service updates the ride details and notifies the driver, with GPS being used to update the driver's route and estimated time of arrival.
- Navigation Engine provides the driver with updated directions to the new destination.
1. Rate Driver
- Rider rates the driver on a scale of 1 to 5 stars after the ride is complete.
- Ride sharing service records the rating and uses it to inform future ride matches, with GPS being used to track the driver's location and route during the ride.
1. Report Issue
- Rider reports an issue with the ride, such as poor driving or unsafe conditions.
- Ride sharing service records the report and investigates the issue, with GPS being used to track the vehicle's location and route during the ride.
1. View Ride History
- Rider and driver can view their past ride history in the app, including the pick-up and drop-off locations, distance, time, fare, and rating, with GPS being used to track the vehicle's location and route during the ride.
1. Manage Account
- Rider and driver can manage their account details, such as payment information and personal information, through the app.
# Functional Viewpoint
# Development Viewpoint
# Deployment View
# Context Viewpoint
# Quality Attribute
# Consistency
# Availability
# Scalability
# Flexibility
# Security
# Performance
# Technical Debt
# Conclusion
# References
# Appendix



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
