# Deidentifying Data
This section provides an example of removing personally identifiable information (PII) from a dataset. There are several ways to "de-identify" data: any processing activities or methods that work to prevent a Data Subject’s identity from being revealed. Two common types of de-identification are "Anonymization" and "Pseudonymization."

**Anonymization** is the process by which Personal Data is rendered *anonymous* so that an individual (or "data subject") is no longer identifiable: it is a permanent change to the data. Common methods include removing personally identifiable information or scrambling values across certain sets of PII.

Example: imagine an organization has survey data that contains fields for name, national ID number, village name, ethnic affiliation, age, education level, and health indicators. In this case, removing name and national ID number would be the first step in making the data anonymous since these "direct attributes" are personal data that directly identify an individual. The "indirect attributes" of village name, ethnic affiliation, age, education level, and health indicators would remain.

However, even though some attributes seem "anonymous" they may not be. If the survey was collected in a very small village where only two residents identify as a particular ethnic affiliation, and they are each different ages, then using those two indirect attributes could allow for those individuals to be identified! The process by which *all* attributes are examined to reduce the risk of re-identifying a data subject is called *Statistical disclosure control*. The first step in this process is a *disclosure risk assessment* and the Humanitarian Data Centre has an [online tutorial for conducting a disclosure risk assessment](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

**Pseudonymization**, on the other hand, describes the processing of personal data in a way that personal data can no longer be attributed to a specific data subject without the use of additional information, such as a key code.

Example: imagine a survey contains your name, email address, age, nationality, and workplace. Pseudonymization takes the data that's identifiable about you specifically (your name, email address, age) and makes it inaccessible and separate from non-identifying data, like your nationality. Pseudonymous data *can* be put back together at some point so that all information can be linked back to a specific source or person. This is why pseudonymization requires that the additional information is kept separately and is subject to technical and organizational measures to ensure that the personal data are not attributed to the data subject.

### Should you choose Anonymization or Pseudonymization?
Anonymizing will generally be safer and reduce the risk of exposing PII. However, this can make the data too general, which may not make it useful for programs such as cash voucher assistance. In the case of health programs that involve vaccinations or other treatments, it may be important to contact individuals for follow-up treatment. In both of these cases pseudonymization would be the best choice since you can always put the data back together to identify an invidual when needed.

**There is no single right answer about when to choose one method over another and it is important to understand why the data were collected, and the needs of the program, before choosing how to deidentify your data.** The techniques used to both anonymize data and to hack data are becoming ever more sophisticated: when in doubt contact you data or IT team for data teams for assistance.

## Importance
 Recent [data breaches at the international Committee of the Red Cross](https://www.icrc.org/en/document/cyber-attack-icrc-what-we-know), [email hacks at the U.S. Agency for International Development](https://www.devex.com/news/usaid-hack-is-wakeup-call-for-aid-industry-on-cybersecurity-100028), and [improper data sharing by the U.N. High Commissioner for Refugees](https://www.hrw.org/news/2021/06/15/un-shared-rohingya-data-without-informed-consent#), show several ways in which humanitarian data are at risk. Data from household surveys, needs assessments and other forms of microdata make up an increasingly significant volume of data in the humanitarian sector. These types of data are critical to determining the needs and perspectives of program participants and the communities we work in, but these data also present risks. Understanding how to assess and manage the sensitivity of these data is essential to ensuring that they are used in a safe, ethical and effective manner in different response contexts.

 Some advantages of using anonymized data over personal data include:
 - protecting against inappropriate disclosure of personal data;
 - fewer legal restrictions apply to anonymized data; and
 - allowing organizations to create open or publicly accessible data while still complying with their data protection obligations.

## Principles
De-identifying data is part of data processing and personal data processing undertaken by humanitarian organizations should comply with the following principles.
- **Fairness and lawfulness of processing**: methods must comply with regional, national, or local legislation or policies that may limit what data can be de-identified and how certain technologies are used. Any processing of personal data should be transparent for the data subjects involved.
- **Purpose limitation**: humanitarian organizations should determine and set out the specific purposes for which data are processed. These purposes
should be explicit and legitimate.
- **Proportionality**: ensure a particular activity related to the processing of personal data is appropriate for the stated goal. For example: is only the minimum required amount of data being collected? Are appropriate technical and organizational measures in place to reduce the risks associated with data processing?
- **Technology changes**: new datasets and new tools for analyzing them change and advance rapidly and so do the means by which data are hacked or stolen. It is important to understand new and emerging risks to your data and continue to adjust your methods and practices accordingly.

## Instructions
You can follow these [Pseudonymization-instructions](Pseudonymization-instructions.md) to walk through a basic example of pseudonymizing a data set. The exercise uses [a sample data set found in the data folder here](data/Pseudonymization_example.csv).

Once you have pseudonymized the sample data, you can continue with the Humanitarian Data Centre's tutorial [for conducting a disclosure risk assessment](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

## Further Assistance
Deidentifying data is part of good data management practices and the larger "data life cycle," or the overall activities for individual data collection as part of a program or response. The following resources are excellent places to start for a more complete understanding of managing your data responsibly.
- The Cash Learning Partnership's *Data Responsibility Toolkit* is designed for cash and voucher practitioners specifically, but is a "gold standard" in guidance for responsible data. The Toolkit is available in [English](https://www.calpnetwork.org/wp-content/uploads/2021/03/Data-Responsibility-Toolkit_A-guide-for-Cash-and-Voucher-Practitioners.pdf), [Arabic](https://www.calpnetwork.org/ar/publication/data-responsibility-toolkit-a-guide-for-cva-practitioners/), [French](https://www.calpnetwork.org/fr/publication/data-responsibility-toolkit-a-guide-for-cva-practitioners/), and [Spanish](https://www.calpnetwork.org/fr/publication/data-responsibility-toolkit-a-guide-for-cva-practitioners/).
- The Electronic Cash Transfer Learning Action Network's [*Data Starter Kit for Humanitarian Field Staff*](https://www.calpnetwork.org/wp-content/uploads/2020/06/DataStarterKitforFieldStaffELAN.pdf) provides a series of data tip sheets for understanding various aspects of good data management and protection practices.
- The International Committee of the Red Cross' [*Handbook on Data Protection in Humanitarian Action*](https://www.icrc.org/en/data-protection-humanitarian-action-handbook) is a detailed guide to almost every aspect of humanitarian data. Chapter 2 specifically deals with deidentifying data.
- The Engine Room's [*Handbook of the Modern Development Specialist*](https://the-engine-room.github.io/responsible-data-handbook/) is a good overview of data in the context of international development activities. The section on [*Sharing Data*](https://the-engine-room.github.io/responsible-data-handbook/chapters/chapter-02c-sharing-data.html) specifically deals with deidentification.
