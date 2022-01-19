# EDA_Bank_Loan_Default_Risk_Analysis 

# 📝 Overview
Introduction This case study aims to give you an idea of applying EDA in a real business scenario. In this case study, apart from applying the techniques that you have learnt in the EDA module, you will also develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

Business Understanding The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter. Suppose you work for a consumer finance company which specialises in lending various types of loans to urban customers. You have to use EDA to analyse the patterns present in the data. This will ensure that the applicants capable of repaying the loan are not rejected.

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

The data given below contains the information about the loan application at the time of applying for the loan. It contains two types of scenarios:

The client with payment difficulties: he/she had late payment more than X days on at least one of the first Y instalments of the loan in our sample,

All other cases: All other cases when the payment is paid on time.

When a client applies for a loan, there are four types of decisions that could be taken by the client/company):

Approved: The Company has approved loan Application

Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan or in some cases due to a higher risk of the client he received worse pricing which he did not want.

Refused: The company had rejected the loan (because the client does not meet their requirements etc.).

Unused offer: Loan has been cancelled by the client but on different stages of the process.

In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.

Business Objectives This case study aims to identify patterns which indicate if a client has difficulty paying their installments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

To develop your understanding of the domain, you are advised to independently research a little about risk analytics - understanding the types of variables and their significance should be enough).

Data Understanding Download the dataset from below.

Dataset Download This dataset has 3 files as explained below:

    1) 'application_data.csv' contains all the information of the client at the time of application. The data is about whether a client has payment difficulties.

    2)'previous_application.csv' contains information about the client’s previous loan data. It contains the data whether the previous application had been Approved, Cancelled, Refused or Unused offer.

    3)'columns_description.csv' is data dictionary which describes the meaning of the variables.

# 💪 Motivation
I started to learn Data science to explore my carrier in Data world. I learned different methodologies and tools to achieve and solve real world problems. Finally it is important to work on application (real world application) to actually make a difference.

# 📀 Installation
The Code is written in Python 3.6.10. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after cloning the repository:

pip install -r requirements.txt

# 🛠⚙ Technology
Windows

Jupyter Notebook/Google Colab/PyCharm

Programming Language: Python

Library: Numpy, Pandas, Seaborn, Matplotlib

# Conclusion
After analysing the datasets, there are few attributes of a client with which the bank would be able to identify if they will repay the loan or not. The analysis is consised as below with the contributing factors and categorization:

## Decisive Factors for an applicant to be Re-payer, hence applications can be approved
AMT_INCOME_TOTAL:Applicants with Income more than 700,000 are less likely to default

CNT_CHILDREN: Applicants with zero to two children tend to repay the loans.

DAYS_BIRTH: Applicants above age of 50 have low probability of defaulting.

DAYS_EMPLOYED: Applicants with 40+ year experience having less than 1% default rate

NAME_CASH_LOAN_PURPOSE: Loans bought for Hobby, Buying garage are being repayed mostly.

NAME_EDUCATION_TYPE: Academic degree has less defaults.

NAME_INCOME_TYPE: Student and Businessmen have no defaults.

ORGANIZATION_TYPE: Applicants with Trade Type 4 and 5 and Industry type 8 have defaulted less than 3%.

REGION_RATING_CLIENT: Applicants who live in areas with Region Rating 1 are safe borrowers.

## Decisive Factors for an applicant to be a potential Defaulter, hence application can be rejected :
AMT_GOODS_PRICE: When the credit amount goes beyond 3M, there is an increase in defaulters.

CODE_GENDER: Male applicants have relatively higher default rate

CNT_CHILDREN : Applicants who have children equal to or more than 9 default 100% and hence their applications can to be rejected.

CNT_FAM_MEMBERS: Applicants who have higher family members (>=11) have higher default rate and their applications can be rejected.

DAYS_BIRTH: Avoid young applicants who are in age group of 20-40 as they have higher probability of defaulting

DAYS_EMPLOYED: Applicants who have less than 5 years of employment have high default rate.

NAME_EDUCATION_TYPE: Applicants with Lower Secondary, Secondary education and incomplete higher education have higher default rate

NAME_FAMILY_STATUS : Applicants in civil marriage or who are single have higher default rate

NAME_INCOME_TYPE: Applicants who are either at Maternity leave or Unemployed have higher default rate.

OCCUPATION_TYPE: Applicants who are Low-skill Laborers, Drivers and Waiters/barmen staff, Security staff, Laborers and Cooking staff as the default rate is huge.

ORGANIZATION_TYPE: Organizations with highest percent of loans not repaid are Transport: type 3 (16%), Industry: type 13 (13.5%), Industry: type 8 (12.5%) and Restaurant (less 
than 12%). Self-employed people have relative high defaulting rate, and thus should be avoided to be approved for loan or provide loan with higher interest rate to mitigate the risk of defaulting.

REGION_RATING_CLIENT: Applicants who live in areas with Region Rating as 3 has highest defaults.

## Decisive attributes for an potential defaulters who can be considered for loan with higher interest to mitigate any default risk to prevent business loss:
AMT_CREDIT: Applicants who get loan for 300-600k tend to default more than others and hence having higher interest specifically for this credit range would be ideal.

AMT_INCOME: Since 90% of the applications have Income total less than 300,000 and they have high probability of defaulting, they could be offered loan with higher interest compared to other income category.

CNT_CHILDREN : Applicants who have 4 to 8 children have a very high default rate and hence higher interest should be imposed on their loans.

CNT_FAM_MEMBERS :Applicants with family members between 8 to 10 have a very high default rate and hence higher interest should be imposed on their loans.

NAME_CASH_LOAN_PURPOSE: Loan taken for the purpose of Repairs seems to have highest default rate. A very high number applications have been rejected by bank or refused by client in previous applications as well which has purpose as repair or other. This shows that purpose repair is taken as high risk by bank and either they are rejected, or bank offers very high loan interest rate which is not feasible by the clients, thus they refuse the loan. The same approach could be followed in future as well.

NAME_HOUSING_TYPE: High number of loan applications are from the category of people who live in Rented apartments & living with parents and hence offering the loan would mitigate the loss if any of those default.

## More suggestions:
90% of the previously cancelled client have actually repayed the loan. Recording the reason for cancellation which might help the bank to determine and negotiate terms with these repaying customers in future for increase business opportunity.

88% of the clients who were refused by bank for loan earlier have now turned into a repaying client. Hence documenting the reason for rejection could mitigate the business loss and these clients could be contacted for further loans.
