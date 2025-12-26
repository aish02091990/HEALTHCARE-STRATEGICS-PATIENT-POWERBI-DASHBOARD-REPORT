**1.Project Overview and Objectives:-**
●	This Project focusing on Patient's Healthcare safety measurement of Data Analysis with excellent quality of healthcare or medical dataset is a collection of health-related information, like Patient records, lab results, medical images, or treatment histories. Healthcare datasets are often organized into data collections, which are curated repositories designed for research, public health, and clinical use.
●	The main objectives of these datasets are used to study human diseases, improve treatments, and develop tools like AI models for better diagnosis and care. Many healthcare datasets contain de-identified health-related data, ensuring patient privacy is protected while still enabling valuable research and analysis.
●	They play a key role in advancing research and improving patient outcomes.
●	Importance of Healthcare Datasets for Training Your Machine Learning Model
 ●	Healthcare datasets are collections of patient information, such as medical records, diagnoses, treatments, genetic data, and lifestyle details.
●	 Data science plays a crucial role in analyzing these healthcare datasets, enabling researchers to uncover insights and drive innovation in patient care. They are very important in today’s world.
________________________________________
**2******.** Data Sources**********
**Source Description and Timeline:Google Dataset Search and 2024-2025
Domain: Patient’s Healthcare/ Countrywise Recovery,Non Recovery/Readmit/Death Strategics Health Related Dashboard Report.**
________________________________________
   **3.Problem Statement** 
●	To determine the patient's health wellness from admission range till Recovery,Non Recovery,re-admission reports such as Age,Gender,count of diseases effects on healthcare through death or recovery Patient history.
●	To study or to identify which country wise, location wise admitted higher or lower risk Related Patients will be diagnosed by various AI- techniques to cure the Patient’s Recovery across the state,country range is the ultimate target for better hospitalisation and staff members support inside healthcare.
●	Evaluating critical patient re-admission records with the correct diagnosis affected should be given higher priority to cure without delay or death ranges.
●	To Analyze for improvements in better recovery ranges and Percentages to cure all types of diseases with good quality and excellent services.
________________________________________
**4.****** Attribute (Column /Features) Details:****  **
Data Type	Description**
 Numeric	Age of the Patient,Gender,ID,Count of Bed.
Categorical / String	Male, Female,Other.
Categorical / String	Rural,Urban,Sub-urban,Country wise,Location wise.
Categorical / String	 Admitted,Recovery,Discharged,Non Recovery,Death.
Death In/Out Patient Record.
Categorical / String	 In and out patient for Recovered\Unrecovered Record.

**5.Tools & Technologies:**
●	 Excel: Data cleaning, transformation, and Pivot Tables.
●	Power BI: Data modelling, DAX calculations, visualization, and interactive dashboard creation.
________________________________________
6. **Data Pre-Processing & Understanding the data (Excel / Power Query)**
Tasks Performed:
●	Data Cleaning & Transformation:Removed duplicates, handled missing values, standardized formats, and created calculated fields.
●	Filtering & Sorting: Organized data to focus on relevant records.
●	Pivot Tables: Generated Pivot Tables for data summarization and initial insights.
●	Convert the data into Fact and Dimension Table.
●	We need to make a separate column for each status of the patient. Divide that column into four categories of Patient - In Patient, Out Patient after recovery and Readmission for non recovery delay hospital cases .
●	The Hospital categories with Patient ID,Gender,Bed occupied location wise country wise ,Bed Unoccupied Patients Percentages along with sum of total staffID occupied .
●	Dropped the Pivot different charts for Healthcare Percentage low,highest which country, location wise described with highest treatment cost for total sum of Patient in occupied /other location wise range .
________________________________________
7.** ****Data Modelling and DAX (Power BI**) ****
●	Data Model: Established relationships between tables, defined cardinality comes under snowflake schema and star schema.
     One to Many Relationship tables along with Many to one,Many to Many Relationship tables.
**DAX FUNCTION FOR HEALTHCARE**
Patients Hospitalised within Particular Time and Year with their Discharge Date.
IF ( ISBLANK ( 'Admissions'[DischargeDate] ) || 'Admissions'[DischargeDate] >= TodayDate, 1, -- Yes, still hospitalised 0 -- No, discharged )
     Diff_Actual_Scheduled DATEDIFF(( 'Admissions'[AdmissionDate], EndDate, DAY)
(COUNTA( 'Admissions' ), 'Admissions'[AdmissionDate] <= SelectedDate)
  IF (ISBLANK ( 'Admissions'[DischargeDate] ),TODAY(), ‘'Admissions'[DischargeDate])
Total Hospitalisation Days = SUM ( Hospital[HospitalisationDays] )
 CALCULATE( SUM (Hospital[HospitalisationDays] ), Hospital[Year] = 2025).
Total Hospitalisation Cost = SUMX ( Hospital, Hospital[Days] * Hospital[CostPerDay] )Hospitalisation Cost = SUM ( Admissions[HospitalisationCost] )
Hospitalisation Cost = SUMX ( Admissions, Admissions[Days] * Admissions[RatePerDay] )
IF(ISBLANK ( 'Admissions'[DischargeDate] ), TODAY(), 'Admissions'[DischargeDate] ) RETURN DATEDIFF ( 'Admissions'[AdmissionDate], EndDate, DAY )
 
8.** **Analysis and Visualizations (Power BI)****
    Data Analysis Observation in Healthcare Record:- 
●	Overall analysis of Patients from Admission ,Recovery/unrecovery,Not Recovery,Repeated cases else Death ,Discharge summary.
●	On time Patient IN/Out Admission Ranges in country location wise.
●	Late Unrecovery,Delayed or Unfortunate Death Range Patient Report.
●	 Patient Highest treatment cost Observed in cliffside country city with Rs73,159. 

**PATIENT’S HEALTH STRATEGICS SUMMARY REPORT**
❖	Inside Hospital before and after Patient admitted IN/OUT Ranges with total number of PatientID with Gender,Treatment cost will be calculated based on each location and Patient room categories ie Normal, ICU,Discharge,Death Summary,Readmitted record observed after Patient admitted in hospital is calculated overall Percentage for Data Visualisation.

**HEALTHCARE STRATEGICS IN/OUT PATIENT VARIATION SUMMARY REPORT**
 **PATIENT IN/OUT VARIATION COUNTRY WISE CITY SUMMARY **
Inside Hospitalisation suppose if the Patient admitted with total number of PatientID  with Gender,Treatment cost will be calculated based on various categories ie Normal, ICU ward,Discharge,Death Summary recorded after Patient IN /OUT Repeatedly with Readmission case due to non recovery in hospital is calculated below in hospital.
 
** PATIENT HEALTHCARETOTAL IN/OUT POWERBI DASHBOARD REPORT**
 
Patient Highest Lowest Comparison Treatment cost Line chart
 
**PATIENT PIVOT CHARTS WITH DASHBOARD REPORT**
****Piechart ****
      Provides the highest count of treatment cost with Langford city indicated with blue color analyzed with Price is 28,652.43 with various sum of age drilled through the Report.

 **STACKED BAR CHART**
 This is a 100%Stacked Bar chart illustrating the total number of Patients admitted in   various city locations with Different colors observed and Patient analysed with Patient  IN with total count with 136 and 290 found with Patient OUT After total safety Health  Recovery.
 
**GAUGE CHART**
This Gauge Chart describes the total headcount of staff working inside healthcare with ER Time mentioned as a total sum of 117283.
 
**DONUT CHART**
The Donut Pivot chart below illustrates country city wise measurement and total treatment highest cost in cliffside city covers overall 73.16k through Data visualisation.
 LINE CLUSTURED COLUMN CHART
Line clustered column chart represents overall Patient’s Age criteria in which  chulavista city found maximum Patient’s Age Line limit falls above ranges with 50k total number count of staffID,Total treatment cost.
**Bubble Chart for Treatment cost Difference Report

**HEALTHCARE IN/OUT PATIENT DIFFERENCE TOTAL REPORT**
9. Insights & Conclusions
Insights: 
**Analysis
●	Overall Healthcare analysis
●	In time or early discharges
●	On time discharges with ER Time
●	Delayed discharges with readmission cases
●	Late discharge with death counts.**
Visualizations based on problem statement:
           **    Month-wise Total early successful Discharge Summary**
Insights:
Out of the total successful discharges 44.24% Patient In/out where early recovery on time in which 53% Patient-out observed with Re-admission cases and remaining 88.49% Late Recovery Patient for Safety Healthcare.
    Total Patient Occupied Bed with Increase and Decrease Variation Report
Insights:
In figure, we can see Patient Admitted with Increase to decreased region wise range across 600% Normal Patient level till ICU Readmission cases found blue color remarks with 800% Safety Patient Recovery in healthcare.
     Healthcare Patient’s Age Variation with Location wise Gender Report
 Summarize trends, patterns, or anomalies identified in the given data for patients IN/OUT with Re-admitted till recovery in healthcare analysis dashboarding Report.
      Key Findings
●	The Patients history shows a clear vision of good health overall in each country allocated across regions, states, and months.
●	Planned staff and team cooperation required for emergency needs without delay.
●	Expert Doctors advanced technology  for quick remedy and impact in high Positive remarks and excellent Quality.
●	Monthly ICU changes or any less ward for patients should not affect in any aspects or happen further for less death ratings.
 Provide the analysis insights:
**Descriptive Analysis:-**
●	What is the overall total number of Summary with Patients in/out/Readmit/Death Percentages observed with high or low difference or major impact after discharges in Healthcare ?
●	The total number of Patients admitted in various city locations with Different colors observed in Patient analysed with IN-Patient total count with 136 and 290 found with Out-Patient After Health Recovery.
●	As Analyzed Inside Healthcare IN-Patient Admission Record found the total                  count of 21 patients Bed occupied status observed overall with Green colour  indicates that Megan F Langford city with less Treatment cost 14.28 as compared with other different city and location wise .
●	Data Visualised with the number of Readmission cases found with the highest level of Range 840.61 with total count of 21 male admitted as compared to Female with less count of 18 members  with 132 Ranges after discharge summary Report.
***
*** Diagnostic Analysis:-******
●	Patients IN Readmitted cases in the dermatology department observed the high level of Percentages for females inside ICU Wards 265.46 as compared to Male Report .
●	Likewise  Patients in recovery for the Cardiology department range covers the highest level in the ICU Room for Male covering overall 929.49 with 49 members found for emergency Purposes. 
●	Male Patients admitted in the Gynaecology department rise to the highest level of Normal with overall Percentages 796.37 with a total 123 counts measured as compared to Female members inside Normal wards.
●	Female inside Neurology department members above 50 age unfortunately death arises with the highest range of 840.61.
    ******Predictive Analytics **
●	OPD OUTPATIENT DEPARTMENT (OPD) observed that certain male oncology diseases found with Discharge summary from normal and icu again these readmitted since un recovery with high count Patient of 20041 Bed aged above 50 with 20083 till recovery time.
●	The below average of 6- 20 ages record states that outpatient recovery after discharge recovery soon becomes outpatient with the given sum of ETR target Time without delay or Readmission Procedure with expected Health Strategics.
 ** Prescriptive Analytics **
●	The Purpose to optimize patient recovery outcomes without delayed Process and Readmitted cases should be analysed for better recovery without Postponed or critical Patient’s death and resources enough to make sure high count of Percentage in ICU Ward can be avoided further for excellent services with latest AI Technology.
●	Recommend early discharge plans and no more readmitted cases for high-risk patients impact on better health strategics and healthcare .
●	Suggesting some New AI Technology for each department to Prevent maximum level of highest ranges of readmitted recovery patients till death circumstances.
●	Optimize bed allocation before to avoid non availability and complaints .  

10**. Conclusions **
     The integration of Excel and Power BI proved effective for end-to-end Patients data analysis, from raw data to visual Report using Excel,PowerBi Technology for each patient's safety measurement and quick Recovery with good Health assurance with excellent services Provided by doctors associated with staff inside each clinic and hospital targets with their own mission and vision and good Quality with Medical challenges undergone with AI Healthcare Latest Technology.


