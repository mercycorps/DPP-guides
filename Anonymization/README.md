# Section Title
This section provides an example of removing personally identifiable information (PII) from a dataset. There are several ways to "de-identify" data: any processing activities or methods that work to prevent a Data Subject’s identity from being revealed. Two common types of de-identification are "Anonymization" and "Pseudonymization."

**Anonymization** is the process by which Personal Data is rendered *anonymous* so that a Data Subject is no longer identifiable. Common methods include removing certain amounts of Personal Data, or applying a range of values across certain sets of Personal Data.

For example, if an organization holds survey data that contains fields for name, national ID number, village name, ethnic affiliation, age, education level, and health indicators, removing name and national ID number would be the first step in making the data anonymous since these attributes are personal data that directly identify an individual. Remember that even though some attributes seem "anonymous" they may not be. If the survey was collected in a very small village where only two residents identify as a particular ethnic affiliation, and they are each different ages, then using those two attributes could allow for those individuals to be identified! The process by which *all* attributes are examined to reduce the risk of re-identifying a data subject is called *Statistical disclosure control*. The first step in this process is a *disclosure risk assessment* and the Humanitarian Data Centre has an [online tutorial for conducting a disclosure risk assessment](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

**Pseudonymization**, on the other hand, describes the processing of personal data in a way that personal data can no longer be attributed to a specific data subject without the use of additional information, such as a key code.

For example, if a survey contains your name, email address, age, nationality, and workplace name, pseudonymization takes the data that's identifiable about you specifically (your name, email address, age) and makes it inaccessible and separate from non-identifying data, like your nationality. Pseudonymous data *can* be put back together at some point so that all information can be taken together and linked back to a specific source or person. This is why Pseudonymization requires that the additional information is kept separately and is subject to technical and organizational measures to ensure that the personal data are not attributed to the data subject.

### Should you choose Anonymization or Pseudonymization?
Anonymizing will always be safer and reduce the risk of exposing PII. However, this can make the data too general, which may not make it useful for programs such as cash voucher assistance. In the case of health programs that involve vaccinations or other treatments, it may be important to contact individuals for follow-up treatment. In both of these cases pseudonymization would be the best choice.

There is no single answer about when to choose one method over another and it is important to understand why the data were collected, and the needs of the program, before choosing how to deidentify your data. The techniques used to anonymize and hack data are becoming ever more sophisticated: when in doubt contact you data or IT team for data teams for assistance.

## Importance
 Recent [data breaches at the international Committee of the Red Cross](https://www.icrc.org/en/document/cyber-attack-icrc-what-we-know), [email hacks at the U.S. Agency for International Development](https://www.devex.com/news/usaid-hack-is-wakeup-call-for-aid-industry-on-cybersecurity-100028), and [improper data sharing by the U.N. High Commissioner for Refugees](https://www.hrw.org/news/2021/06/15/un-shared-rohingya-data-without-informed-consent#), show several ways in which humanitarian data are at risk. Data from household surveys, needs assessments and other forms of microdata make up an increasingly significant volume of data in the humanitarian sector. These types of data are critical to determining the needs and perspectives of people affected by crises but also presents risks. Understanding how to assess and manage the sensitivity of these data is essential to ensuring that they are used in a safe, ethical and effective manner in different response contexts.

## Principles - finish
"As covered in Tipsheet 3, Data Minimization is a core principle of responsible data management. One way to minimize the amount of personal or sensitive data that you are holding is to de-identify it. In other words, to remove identifying information so that the data becomes ‘anonymous’. When data is anonymized or de-identified, the association between data and the individuals to which it relates is removed so that an individual cannot be identified in the data. This is done by removing both ‘direct identifiers’ and ‘indirect identifiers’, for example, by removing a national ID number or a birthdate. This process makes the data more private and puts people at less risk because it has been scrubbed of identifying information or aggregated to a level where individuals cannot be identified.**These 2 paragraphs from Linda**

Advantages of using anonymized data where appropriate over personal data include:
- it protects against inappropriate disclosure of personal data;
fewer legal restrictions apply.
- it can be easier to use anonymised data in new and different
ways because the DPA’s purpose limitation rules do not apply;
- it allows organisations to make information public while still
complying with their data protection obligations; and
- the disclosure of anonymised data is not a disclosure of personal data – even where the data controller holds the key to allow reidentification to take place.

## Instructions or Guidance - finish
As needed per section.
Exercise here: https://www.excel-exercise.com/anonymise-your-data/
Create data set.

## Further Assistance - finish
Link out to other resources. Especially those on data minimization...
ELAN on various forms of Encryption
