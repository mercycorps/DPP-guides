# Section Title
This section provides an example of removing personally identifiable information (PII) from a dataset. There are several ways to "de-identify" data: any processing activities or methods that work to prevent a Data Subject’s identity from being revealed. Two common types of de-identification are "Anonymization" and "Pseudonymization."

**Anonymization** is the process by which Personal Data is rendered *anonymous* so that a Data Subject is no longer identifiable: it is a permanent change to the data. Common methods include removing personally identifiable information or scrambling values across certain sets of PII.

For example, if an organization holds survey data that contains fields for name, national ID number, village name, ethnic affiliation, age, education level, and health indicators, removing name and national ID number would be the first step in making the data anonymous since these "direct attributes" are personal data that directly identify an individual. The "indirect attributes" of village name, ethnic affiliation, age, education level, and health indicators would remain.

Remember that even though some attributes seem "anonymous" they may not be. If the survey was collected in a very small village where only two residents identify as a particular ethnic affiliation, and they are each different ages, then using those two indirect attributes could allow for those individuals to be identified! The process by which *all* attributes are examined to reduce the risk of re-identifying a data subject is called *Statistical disclosure control*. The first step in this process is a *disclosure risk assessment* and the Humanitarian Data Centre has an [online tutorial for conducting a disclosure risk assessment](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

**Pseudonymization**, on the other hand, describes the processing of personal data in a way that personal data can no longer be attributed to a specific data subject without the use of additional information, such as a key code.

For example, if a survey contains your name, email address, age, nationality, and workplace name, pseudonymization takes the data that's identifiable about you specifically (your name, email address, age) and makes it inaccessible and separate from non-identifying data, like your nationality. Pseudonymous data *can* be put back together at some point so that all information can be taken together and linked back to a specific source or person. This is why Pseudonymization requires that the additional information is kept separately and is subject to technical and organizational measures to ensure that the personal data are not attributed to the data subject.

### Should you choose Anonymization or Pseudonymization?
Anonymizing will always be safer and reduce the risk of exposing PII. However, this can make the data too general, which may not make it useful for programs such as cash voucher assistance. In the case of health programs that involve vaccinations or other treatments, it may be important to contact individuals for follow-up treatment. In both of these cases pseudonymization would be the best choice.

There is no single answer about when to choose one method over another and it is important to understand why the data were collected, and the needs of the program, before choosing how to deidentify your data. The techniques used to anonymize and hack data are becoming ever more sophisticated: when in doubt contact you data or IT team for data teams for assistance.

## Importance
 Recent [data breaches at the international Committee of the Red Cross](https://www.icrc.org/en/document/cyber-attack-icrc-what-we-know), [email hacks at the U.S. Agency for International Development](https://www.devex.com/news/usaid-hack-is-wakeup-call-for-aid-industry-on-cybersecurity-100028), and [improper data sharing by the U.N. High Commissioner for Refugees](https://www.hrw.org/news/2021/06/15/un-shared-rohingya-data-without-informed-consent#), show several ways in which humanitarian data are at risk. Data from household surveys, needs assessments and other forms of microdata make up an increasingly significant volume of data in the humanitarian sector. These types of data are critical to determining the needs and perspectives of people affected by crises but also presents risks. Understanding how to assess and manage the sensitivity of these data is essential to ensuring that they are used in a safe, ethical and effective manner in different response contexts.

 Some advantages of using anonymized data over personal data include:
 - protecting against inappropriate disclosure of personal data;
 - fewer legal restrictions apply to anonymized data; and
 - allowing organizations to create open or publicly accessible data while still complying with their data protection obligations.

## Principles
- Data Minimization is a core principle of responsible data management and one way to minimize the amount of personal or sensitive data that you manage is to de-identify it.
- De-identification methods must comply with regional, national, or local principles: be aware that some country-specific and local legislation or policies may limit what data can be de-identified and how certain technologies are used.
- Technology changes: new datasets, and new tools for analyzing them change and advance rapidly. It's important to understand new and emerging risks to your data and continue to adjust your methods and practices accordingly.

## Instructions or Guidance - finish
The following instructions walk through a basic example of pseudonymizing a data set. Begin the exercise here. **Exercise here: https://www.excel-exercise.com/anonymise-your-data/
Create data set.**

To further ensure that the data set are fully anonymized, continue with the Humanitarian Data Centre's tutorial [for conducting a disclosure risk assessment](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

## Further Assistance - finish
it's complex, you need to learn more... start here...
