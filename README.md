# Familial Breast Cancer Initial Risk Assessment Tool

## Table of Contents
- [Project Overview](#project-overview)
- [Prerequisite Knowledge](#prerequisite-knowledge)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Risk Level Function](#risk-level-function)
- [Results Interpretation](#results-interpretation)
- [Limitations](#limitations)
- [References](#references)
- [Contact](#contact)


### Project Overview
---
Breast cancer recovery is high if there is early detection. The main purpose of this DSS (Decision Support Systems) is to focus on early detection through breast cancer in the family. This DSS is not a diagnosis for breast cancer. It is an initial risk assessment tool. The DSS emphasise on individual risk of breast cancer that occurs within families, where multiple relative are affected by the disease. The DSS is knowledge based and uses the NICE guideline for familial breast cancer.

![results1](https://github.com/user-attachments/assets/b943c986-0212-4251-90d6-96426519b80d)


### Prerequisite Knowledge  
To effectively use the app, the user must have knowledge of her first-degree or second-degree relatives. First-degree relatives as stated in the NICE guideline include mother, father, daughter, son, sister, brother. Second-degree relatives also include grandparent, aunt, uncle, niece, nephew, half-sister, half-brother.

### Usage
1. Filling the form by ticking Yes or No

![bc1](https://github.com/user-attachments/assets/c85573cc-b9a5-4759-b4f3-48a5135a05ab)


![bc2](https://github.com/user-attachments/assets/44cd4d80-74a2-4de4-89bb-72c926c02f7a)


![bc3](https://github.com/user-attachments/assets/eca4e536-a260-42a0-9915-d2aed0828be4)

3. After filling the form, click on submit for the results

### Technologies Used
- R - Programming language for statistical computing and graphics
[Download here](https://posit.co/products/open-source/rstudio/)

- Shiny - R package for building interactive web applications
[Click here](https://www.shinyapps.io/)

### Risk Level Function
```r
    # Function to get risk status and message
    get_risk_status <- function(sum) {
      if (breast_cancer_risk(sum) >= 30) {
        risk_status <- "HIGH RISK."
        message <- "For this level of risk, 300 or more women in every 1,000 will \n develop breast cancer. \nBook an appointment with your GP for breast cancer screening."
      } else if (breast_cancer_risk(sum) > 17) {
        risk_status <- "Moderate risk."
        message <- "For this level of risk more than 170 but fewer than 300 women in every \n 1,000 will develop breast cancer. \nBook an appointment with your GP for breast cancer screening." 
      } else {
        risk_status <- "General population risk."
        message <- "For this level of risk, 110 women in every 1,000 will develop breast cancer. \nBook an appointment with your GP for breast cancer screening."     
      }
      return(list(risk_status = risk_status, message = message))
    }
```


### Results Interpretation

![results1](https://github.com/user-attachments/assets/317ffef1-2018-47ef-bdd0-0c444507e72d)

![results2](https://github.com/user-attachments/assets/eff2fc28-dfa5-465d-8237-42c6dcbb1fb5)

![results3](https://github.com/user-attachments/assets/5e4461f1-10fc-496e-9cfe-2db24371564f)


### Limitations
The algorithm used in this Decision Support System (DSS) is currently biased toward a single breast cancer risk factor — family history. Other important risk factors, such as genetics, age, age at first menstrual period, and age at first childbirth, were not considered during the coding process. These additional factors could be incorporated in future improvements to enhance the system’s accuracy and reliability.

### References

1.	Breastcanceruk. (2024) Reduce Your Risk. Breast Cancer UK. [Online] Available from: https://www.breastcanceruk.org.uk/reduce-your-risk/. [Accessed 10 May 2024].
2.	Cancer Matters Wessex. (2024) Breast screening. [Online] Available from: https://cancermatterswessex.nhs.uk/cancer-screening-and-prevention/screening-for-breast-cancer/. [Accessed 15 April 2024].
3.	NHS Digital. (2023) Building healthcare software - clinical coding, classifications and terminology. [Online] Available from: https://digital.nhs.uk/developer/guides-and-documentation/building-healthcare-software/clinical-coding-classifications-and-terminology. [Accessed 10 May 2024].
4.	NICE. (2013) Familial breast cancer (breast cancer in the family). [Online] Available from: https://www.nice.org.uk/guidance/cg164/ifp/chapter/Information-about-risk-of-familial-breast-cancer. [Accessed 6 May 2024].
5.	Scriven, S. (2022) What is Clinical Coding?. [Online] Available from: https://www.fedip.org/post/what-is-clinical-coding. [Accessed 10 May 2024].


## Contact
Feel free to reach out!  
📧 Email: [oduroprince08@gmail.com](mailto:oduroprince08@gmail.com) &nbsp;|&nbsp; 🔗 LinkedIn: [linkedin.com/in/oduroprince24](https://linkedin.com/in/oduroprince24)


🚀
📊
📈
🧠

Thanks for visiting! 😄

