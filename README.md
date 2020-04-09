# staysafe-shielding
Covid-19 StaySafe shielding project



## Personas


Premise: there is a backend ("COC") that menages comunication with apps.
Apps are identified by an ID ("COC_ID") 
There is another backend that menages staysafe-cordone sanitario system.


### SDK Personas

#### Albert the App Business Owner

Albert is 48, he's the owner of a successful small software company. He has developed websites, web applications and mobile applications for customers all over Europe. He's been very successfull on the market and his company is considered a leader for mobile development. His company's operations haven't been disrupted by SARS-CoV-2 but is worried that the economic downturn following the epidemic could severly impact his business. He believes that the usage of tracing technology could help the socity to recover more rapidly and keep it working while waiting for more definitive solutions to the disease.

##### Goals
Albert would like to create an application to help with contact tracing and wants to use his company experience in building mobile apps to 

##### Values and Fears

Albert cares about:
- helping the local community through using his company know how
- consolidating his company position as a leader in his market

She is afraid of:
- Being cut-out from the upcoming platform
- Having a solution that is not privacy compliant because of the interoperability platform
- Having an application that has security issues
- Being unable to anticipate the shifts in the digital and mobile apps market

#### Alice the App Product Owner

##### Details

Alice is 31, she’s a product manager for digital companies. She has worked mostly on B2C facing online services and consumer mobile apps. She wants to crafti applications that are easy to use and pleasant and wants to create experiences that users love. When her current company owner had started exploring the idea of developing a contact tracing application for SARS-CoV-2 she has jumped right into the opportunity since she feels that it could be a great way to make an impact. She also believes that developing an effective application will require a deep understanding of end users and how to build great UXes

##### Goals
Alice would like to create an application that is easy for its users as it believes that this is the best way to drive the usage and make it effective.

##### Values and Fears

Alice cares about:
- having the freedom to build the best user experience 
- being able design a responsive application for both Android and iOS phones

She is afraid of:
- Having to design cumbersome user onboarding and identification flows
- Being limited with the way the app should be designed


#### Bob the App Developer

##### Details

Bob is 25, he’s an experienced mobile software developer. He has worked with a few different companies as a freelancer and helped to create apps for both Android and iOS ecosystems. His current company has decided to participate in the development of a contact tracing application that integrates into the Staysafe platform and he has been tasked with integrating the SDK. He is expert in  native development but lately moved to cross-platform tools to improve the time-to-market and have a common codebase across both mobile app stores. 

##### Goals
Bob would like to integrate the SDK into his workflow as painlessly and rapidly as possible. To do so he would like to be able to keep using the mobile app stack he has standardized on which is based on React Native.

##### Values and Fears

Bob cares about:
- building applications that are successful and high quality in terms of user feedback on the app stores
- being efficient in coding the application, and being able to code [Alice](#alice-the-app-product-owner) requirements
- being able to easily track down errors and issues, specially with with external SDKs

He is afraid of:
- Having to battle with unclear or lacking documentation
- Being unable to build the application using his current tools
- Having to use an SDK with bugs and unexpected behaviours

that take advantage of the device features
that can be monetized well (they rely on in-app purchases)
that are responsive to the user input
that work on phones and tablets


### End Users

#### Marco the Immune Volunteer

##### Details

Marco is 34, he’s a proactive with strong civic sense. He was diagnosed with SARS-CoV-2 but has now fully recovered. He is keen to get back to work soon after a long quarantine. In the spirit of helping his local community he has taken steps to become a volunteer and provide care to fragile elderly. He knows how to use a smartphone, but technology isn’t really his thing.

##### Goals
Marco would like to get the “volunteer” certification so that he could go ahead and start helping his community. He is looking for the fastest and simplest way to achieve this goal.

##### Values and Fears

Marco cares about privacy in general and doesn’t want to be tracked or share his data with any large government or corporation</br>
He is afraid of:
- Carrying the virus to the fragile people he is helping
- Being tracked and observed in his daily life
- Not knowing how to use the application properly

#### Paola the Pharmacist

##### Details

Paola is 47, living in Milano, she’s been working in her pharmacy with her husband for over 12 years. She’s open minded and relaxed, taking life one step at a time. She hasn’t been tested for SARS-CoV-2, but none of his relatives was exposed so fairly confident of not being infectious.

##### Goals
Paola's goal is to get back to “business as usual" as soon as possible. Her family depends on the pharmacy business. She’s now one of the few registered professionals that can test the virus antibodies and produce digital certificates for immunity. While she’s happy to contribute to solving the current crisis, her major interests stay with the pharmacy itself.

##### Values and Fears

Paola cares about her community, and especially their health. She’s afraid the current situation will be prolonged and that everyone will suffer, if not due to health conditions and access to treatment, due to the economic impact that this crisis will have.

#### Walter the Institutional Force

##### Details
Walter is 51, he works with the Civil Defence forces and he is in charge of coordinating volunteering efforts in a large province with a population of 1.2M people.

##### Goals
Walter wants to leverage all existing resources to mitigate the damages of the current epidemic. Supporting all those in need with essentials and protective equipment. He needs to recruit the most immune volunteers possible to serve the local population.

##### Values and Fears
He fears to unknowingly spread the virus while trying to mitigate its damages. While he values privacy, he needs technological aid to gain visibility and make quick decisions.


#### Franca the Fragile Person

##### Details
Franca is 72, already home-bound due to the government directions to the elderly. She’s getting essentials delivered at home by either supermarkets or volunteers. Living alone, with no family within her city she needs external support to survive.

##### Goals
Survive. She needs to rely on low-tech communication, not having a computer and having only limited experience on how to use her smartphone.

##### Values and Fears
Franca fears to be “left behind” and to have little means to request help/support.


#### Andrea the lorry driver
##### Details
Andrea is 51, she is from Poland. She drives a lorry for work. Sometimes she has to travel across countries to deliver goods.

##### Goals
Andrea's goal is to get back to “business as usual" as soon as possible. Her family depends on the pharmacy business.
##### Values and Fears
She fears that she might lose her job in case travel across Europe is restricted.
Some countries may deny her access, even though she could be immune.


#### Natasha CEO of Lorry for women.
##### Details
Natasha is 43, she owns the comapany where [Andrea](#andrea-the-lorry-driver).
##### Goals
She has been hit hard by the crisis, so she needs to get back to "business as usual" as soon as possible.
##### Values and Fears
- She fears that due to travel restrictions her business might go under.
- She fears that her employees might be endangered, phisically and economically.


## User Stories

### [US8] Proof of Immunity

#### Conditions

##### Precondition
Marco’s state is immune

#### Story
Marco is asked by
[Walter](#walter-the-istitutional) to prove that his state is immune. Marco opens the mobile app and authenticates. The app shows a QR code that contains Marco’s COC_ID. [Walter](#walter-the-istitutional) scans the QR code using the operator app. The operator app checks Marco’s state on the backend (including the expiration date if the state is immune), and returns it to [Walter](#walter-the-istitutional).

### [US9] Marco Volunteers to Join Cordone Sanitario
##### Precondition
Marco’s state is immune
#### Story
Marco goes to Walter at
protezione civile, and volunteers to join cordone sanitario for
at-risk individuals. Marco proves that he is immune as described in
US8. [Walter](#walter-the-istitutional) registers [Marco](#marco-the-immune-volunteer)’s information, including his COC_ID and
photo, to protezione civile’s system. Protezione civile’s system
uses the COC backend to send a notification to [Marco](#marco-the-immune-volunteer) mobile
app. [Marco](#marco-the-immune-volunteer) authenticates in front of [Walter](#walter-the-istitutional), and the app records
[Marco](#marco-the-immune-volunteer) as a volunteer.





### [US10] Marco’s Immunity Expires
##### Precondition
Marco’s state is immune.
##### Post-condition
 Marco’s state is unknown
 #### Story
The mobile app notifies [Marco](#marco-the-immune-volunteer)  that his state has expired, and
that it is now unknown. [Marco](#marco-the-immune-volunteer)  can now proceed with US1.






### [US11]  Marco is Tested (Tampon).
 ##### Precondition
  [Marco](#marco-the-immune-volunteer) state is unknown, immune, or negative.
 ##### Post-condition
  [Marco](#marco-the-immune-volunteer) state is quarantined, negative, or immune
#### Story
 [Marco](#marco-the-immune-volunteer) feels
sick, and goes to his doctor Giovanni. Giovanni records information
about the test using the operator app, and updates [Marco](#marco-the-immune-volunteer)’s
state to unknown - thus possibly revoking [Marco](#marco-the-immune-volunteer)’s immune
state. After a few days, the test result is back. If the test is
positive, [Marco](#marco-the-immune-volunteer)’s state becomes quarantined. If the test is
negative, [Marco](#marco-the-immune-volunteer)’s state is set to negative or immune,
depending on [Marco](#marco-the-immune-volunteer)’s state at the beginning of US11.






### [US12] Marco Visits Franca.
##### Precondition
 Marco’s state is immune
 #### Story
[Walter](#walter-the-istitutional) sends Marco to [Franca](#franca-the-fragile-person). Marco knocks [Franca](#franca-the-fragile-person)’s door, and
[Franca](#franca-the-fragile-person) asks him to identify himself. Marco authenticates with the
mobile app on his smartphone, which then broadcasts Marco’s
certified COC_ID over Bluetooth LE. [Franca](#franca-the-fragile-person)’s app scans Bluetooth
devices and read’s Marco’s COC_ID using the mobile app on
her smartphone. [Franca](#franca-the-fragile-person)’s mobile app sends the COC_ID to the
backend, which returns Marco’s photo if his state is immune
and he was registered by [Walter](#walter-the-istitutional). Otherwise, the mobile app tells
[Franca](#franca-the-fragile-person) not to open the door. The backend records the interaction
between Marco and [Franca](#franca-the-fragile-person). [Franca](#franca-the-fragile-person) verifies that Marco matches the
photo shown on her mobile app, and opens the door.



### [US13] Antibodies test

#### Conditions

##### Precondition
Marco’s state is unknown

#### Story
Marco goes to [Paola](#paola-the-pharmacist) in order to perform an antibodies test.
If the test is positive [Paola](#paola-the-pharmacist) ask for Marco's tax code and phone number and records them using operator app.
The operator app notifies the institutional forces.


Otherwise [Paola](#paola-the-pharmacist) informs [Marco](#marco-the-immune-volunteer) that she can add the test-certificate on his user app if he wants. 
[Marco](#marco-the-immune-volunteer) can open the user-app that generates a QRcode (QRcode=f(timestamp,COC_ID)), [Paola](#paola-the-pharmacist) uses the operator-app to read the QRcode. After that she selects the test result (negative or immune) and the operetor app sands the information to the backend.

The information are stored in a db, morover they are sended to COC Backend that forwards the certificate to the user-app.
The certificate will be stored [Marco](#marco-the-immune-volunteer)'s device memory.


### [US14] expired immunity

#### Conditions

##### Precondition
[us13] [Marco](#marco-the-immune-volunteer) has a test-certificate

#### Story
The test-certificate has an expiring-date. After this date [Marco](#marco-the-immune-volunteer) has to go back to [Paola](#paola-the-pharmacist) in order to update his immunity condition.

### [US15] Marco is a bad person

#### Conditions

##### Precondition
[Marco](#marco-the-immune-volunteer) has a test-certificate

#### Story
When [Marco](#marco-the-immune-volunteer) goes to [Franca](#franca-the-fragile-person) robs her. Franca reports the crime to Carabinieri. Pietro, the policeman, uses the user-app to read [Franca](#franca-the-fragile-person) COC_ID, then He asks to Stefano, the app owner, [Marco](#marco-the-immune-volunteer)'s COC_ID stored in [Franca](#franca-the-fragile-person)'s contact logs. Pietro, the policeman, asks to [Walter](#walter-the-istitutional) to revoke [Marco](#marco-the-immune-volunteer)'s volunteer certificate.


### [US16] Natasha encourages her employees to take the test
#### Conditions
##### Precondition
#### Story
Natasha wants to do business in Italy knowing that crossing the border is permitted only if her drivers have a certification of immunity. She encourages her employees to take the test and obtain permission to cross.

### [US17] Andrea corsses the italian border
#### Conditions
##### Precondition
Marco’s state is immune.
[US16] Natasha encourages her employees to take the test
#### Story
Following Natasha's advice she takes the immunity test and obtains the certification.
Now she can cross the Italian boarder.
At the border she authenticate herself using the user application and the COC_ID.
[Walter](#walter-the-istitutional) grants her access.


## User Stories (in detail)

### Marco – Volunteer

- **M1 – Volunteer Onboarding**
As a Volunteer, Marco wants to get registered quickly and smoothly so that he can start to help as soon as possible. 

- **M2 – Volunteer Immunity Certification Registration**
As a Volunteer, Marco needs to get a certification of his immunity and be able to display it upon request so that those he interacts with can trust him. 

- **M3 – Volunteer Immunity Certification Renewal**
As a Volunteer, Marco wants to renew his immunity certification smoothly and effectively so that he can carry on working as volunteer. 

- **M4 – Volunteer Immunity Certification Cancellation**
As a Volunteer, Marco needs to know if/when his immunity certification is cancelled or will expire so that he can either renew it or change his behavior effectively.

- **M5 – Volunteer Registration with Authorities**
As a Volunteer, Marco wants to register as a Volunteer with the Authorities so that he can start helping out. 

- **M6 – Volunteer Recognition**
As a Volunteer, Marco needs to be easily recognizable (especially by fragile / high-risk citizens) so that he can perform his duties effectively. 


### Paola – Pharmacist

- **P1 – Sanitary Personnel Onboarding**
As a Pharmacist, Paola wants to download and use the App easily so that she can start to add certifications and test results.
- **P2 – Sanitary Personnel Antibodies Test Submission Registration**
As a Pharmacist, Paola wants to register the submission of an Antibodies test via the App (including the test subject ID) so that all data are shared and up to date.
(maybe using the sanitary card if possible).
- **P3 – Sanitary Personnel Antibodies Test Results Registration**
As a Pharmacist, Paola wants to register the Antibodies Test results updating the registration submission easily with the least amount of effort so that she can go back to work. 
- **P4 – Sanitary Personnel Immunity Registration***
As a Pharmacist, Paola wants to issue an Immunity Certification seamlessly after receiving a positive result on an Antibodies test so that the test subject is immediately alerted and can start working or helping others. We can consider the “positive antibodies test” registration as the element that triggers automatic certification.
- **P5 – Sanitary Personnel Immunity Renewal***
As a Pharmacist, Paola wants to renew an Immunity Certification as quickly as possible after receiving test results. We can consider a further “positive antibodies test” registration as the element that triggers automatic renewal of the Immunity Certification.
- **P6 – Sanitary Personnel Immunity Revocation***
As a Pharmacist, Paola wants to revoke an Immunity Certification by updating a Virus Test result or due to the subject showing symptoms of Covid-19.



*Immunity status should be tied to tests performed and the results of those tests should affect the immunity status directly, without leaving the Pharmacist any direct control on the certification status control. We should also consider what test details we want/can include in the system.

### Walter – Institutional Forces

- **W1 – Institutional Forces Onboarding**
As part of the Institutional Forces, Walter wants to download and use the App on his phone quickly and easily so that he can start using it. 
- **W2 – Institutional Forces Citizen Status Check**
As part of the Institutional Forces, Walter needs to check the status of a Citizen so that he could make decisions effectively.
- **W3 – Institutional Forces Volunteer Status Check**
As part of the Institutional Forces, Walter wants to check the immunity status of a Volunteer so that he could register him/her as Volunteer or make related decisions. 
- **W4 – Institutional Forces Volunteer Registration**
As part of the Institutional Forces, Walter wants to register a Volunteer (who is immune) effectively with few clicks on the App so that she/he can start working soon. 
- **W5 – Institutional Forces Volunteer Management**
As part of the Institutional Forces, Walter wants to be regularly updated on the status of all Volunteers and forces under his management so that he can ensure a high quality and efficacy of his services.

### Franca – Fragile Population

-	**F1 – Fragile Population Onboarding**
As part of the Fragile Population, Franca wants to get access to the services but struggles to use digital devices. She needs step by step guidance on how to access, download and use the app (or something more rudimental) so that she can request and receive support.
-	**F2 – Fragile Population Volunteer Recognition**
As part of the Fragile Population, Franca needs to recognize a Volunteer when he/she reaches out to her to deliver goods or services so that she is safe. 
-	**F3 – Fragile Population FeedBack**
As part of the Fragile Population, Franca needs to express her pleasure/displeasure of the service provided.

## Functionalities
### User App
- **Autentication**
- **User certification lookup**
- **User test lookup**
- **Request help**
- **Receive volunteer autentication**
### Operator App (Volunteer)
- **Autentication**
- **User certification lookup**
- **User test lookup**
- **Request help**
- **Reply to help request**
- **Confirm autentication**
### Operator App ( Sanitary Personnel )
- **Autentication**
- **Certificate creation**
- **Certificate update**
- **Certificate removal**
- **Test creation**
- **Test results publication**


## Certificate
The immunity certificate must contain the following info:
```
<certification id>
<test id>
<manifacturer id>
<lot id>
<identificativo entità che lo ha effettuato>
<DB url where test data are stored>
<Sanitary Personnel id, who submitted the test>
<test timestamp>
<test type (PCR, IGG, IGM)>
<test outcome>
<Identity document number>
<Identity document type>
<Identity document issuer>
```
When a user wants to prove his/her immunity has to show a QRcode that contains these informations
```
<DB url where test data are stored>
<test type (PCR, IGG, IGM)>
<test outcome>
<Identity document number>
<Identity document type>
```

## Issues
- Virus test is different from antibodies test, which one should we consider for specification purposing? Both?
- The QRcode is generated upon onboarding or upon test result?
- Should the volunteer have a specific certification that proves its status, or is the status just an information stored on the DB?
- How the sanitary personnel are enrolled? Is it a metter of the application or someone else?
- Does a test machine update the test outcome in real time on the db? If so, is it a matter of the application or the backend should provide a sicure call to update test results?