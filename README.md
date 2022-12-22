# Team-Rueeblimaert-Aarau
## Members

- Leena Anthony
- Aletta Karsies
- Paul Stehberger
- Andreas Heule

## Introduction

In Switzerland, drugs with medical promise are usually sold and handed over to the patient in pharmacies. Depending on the category of a drug a prescription by a medical doctor is needed.

In our project, we focus on the interaction between the medical doctor in a practice or hospital who fills the drug prescription and the pharmacy, as well as the process in the pharmacy where the prescription is checked and the required drug is eventually sold.

In today's common practice medical doctors and pharmacies both store the prescription information in their respective information systems which are **not** connected. Sending a prescription from a doctor's practice to the pharmacy is mostly done via email or on paper. In addition, there is no common database containing the patient's complete medication history.

## Our Goal

We want to digitalise the procedure and the handling of prescriptions and therefore gain more efficiency for pharmacies. One other positive effect is going to be the improvement of drug interaction checks for patients.  
The prescription will be sent to the pharmacy by filling out a Google form. The pharmacy receives the order and sees the current medication of the patient. With a decision table the medication will be checked for drug interaction. The pharmacist then double checks the data. After that, depending of the check result, the patient will be informed by email to kindly pick up their medication, or the prescribing physician will be informed about the detected drug interaction by email.

![image](https://user-images.githubusercontent.com/115709957/209010933-959bf8d1-bb6a-4d2a-9c92-da9564c3c892.png)


## List of Assumptions

- To simplify our project the patient can only choose from two pharmacies **A** and **B**
-	The used Google documents are secure and personal data will not leak
-	Our Google sheet has the same function as a database
- The decision table is simplified and would be replaced with a software approved by SwissMedic. We also do not distinguish between drug name and active ingredient
- All user tasks will be handled directly by the employees of the pharmacy.

## Start of the Process:

In our digitalised process, the patient goes to a physician. If needed the medical doctor writes a prescription by filling out the [Google form][1] (ten questions). Our BPM process starts as soon as the physician sends the Google form. In the screenshots below is an example of our Google form.

[1]: https://docs.google.com/forms/d/e/1FAIpQLSfqVcNNJvv8UbSqdx3HZtLKWscjcq13AHXkysQsV_cB3ej1MA/viewform
![image](https://user-images.githubusercontent.com/115709957/209001835-aad677fd-aff0-4c5e-b1d3-844213653510.png)

By sending the Google form, a new row is automatically inserted in the [Prescription Form (Responses)][2].

[2]: https://docs.google.com/spreadsheets/d/1xP-jTlqB5-bax8qxv7f1s43OcnDquWo0AHF_OP_aLEc/edit#gid=1636714263

![image](https://user-images.githubusercontent.com/115709957/209001861-63387c09-e27e-40cc-b552-2ce6e6a32de7.png)

## Pharmacy A or Pharmacy B
By choosing **Pharmacy A** or **Pharmacy B** in the google form. Our first make scenario (*Pharmacy_Scenario1_Task1.json*) will send the data to either **Pharmacy A** or **Pharmacy B**.

![image](https://user-images.githubusercontent.com/115709957/209001900-3ed89301-9fc3-4b4d-b506-2e13b30b0221.png)

The Router will filter the data for *Pharamacy A* or *B* and then pass it along to the right Pharmacy

![image](https://user-images.githubusercontent.com/115709957/209001948-df0d4acf-8b5d-46f6-8c3e-5b05f61759f6.png)

By choosing **Pharmacy A** and sending the Google form. The process is then automatically initiated in *Pharmacy A*, as you here can see:

![image](https://user-images.githubusercontent.com/115709957/209001997-b57b0000-bd0c-4d2b-b819-7fd4b736b58a.png)

Then the data will be sent back to comunda and the process is initiated in Pharmacy A.

## Drug interaction
After claiming the task, the second make scenario (*Pharmacy_Scenario2_GetMedicationList.json*) will summarise all entries from the patient ID in the *prescription form* so we get the patients medical history.

![image](https://user-images.githubusercontent.com/115709957/209002041-92716fb0-dc5d-430e-b7d2-db0b8903b8c5.png)

The *google sheet* will select only the data of the current *Patient* (Patient ID)
![image](https://user-images.githubusercontent.com/115709957/209002059-38188e99-f47c-4e14-ac19-efb56850bdd4.png)

The first *Tool* is going to summarise all data (green boxes) into one text separated by a semicolon:

![image](https://user-images.githubusercontent.com/115709957/209002076-fc30e509-9adb-4b1e-ab24-cd61765b9696.png)

The second *Tool* puts all selected data into a new variable value called *MedicationRecord* to later on search for drug interactions. 

![image](https://user-images.githubusercontent.com/115709957/209002155-d18210f1-840d-4e09-9697-6f8a545e9f7b.png)

The *MedicationRecord* will now be send back to comunda. Here you see the *MedicationRecord*:

![image](https://user-images.githubusercontent.com/115709957/209002192-fe4cd3e0-738c-46a9-b9e3-8fbf42a5b78a.png)

The *User Task* **View MedicationList** is now activated
![image](https://user-images.githubusercontent.com/115709957/209002225-e2b43dcd-a031-4c59-9288-9dfc32a36c2b.png)



Now our decision table will search for drug interaction. If it finds a drug combination which could have a interaction. The Process will have the output *no drug interaction* (green) or *a drug interaction* has been detected (red)
![image](https://user-images.githubusercontent.com/115709957/209002255-6a2446d5-12c5-4b01-95ff-35bec9754c67.png)

The pharmacist will now see the *User Task* **View Drug Interaction Report**

![image](https://user-images.githubusercontent.com/115709957/209002242-8df6160b-c570-4697-97d2-37efae24cec4.png)

The pharmacist is now able to double check the decision made by the decision table and can verify (complete) the task.

![image](https://user-images.githubusercontent.com/115709957/209002279-2509f8f1-d1c8-477c-9d0b-bfaa34a3603c.png)

 Because there was **NO** drug interaction noticed, employees of the pharmacie A will be preparing the medicine for the patient.
 
![image](https://user-images.githubusercontent.com/115709957/209002298-86c4577a-ed93-4a6d-9398-390e52d3bfc4.png)

 The 4th make scenario (*Pharmacy_Scenario4_PrescriptionReady.json*) will now send an email to the patient to inform them to pick up their medicine.

![image](https://user-images.githubusercontent.com/115709957/209002318-0fa33eb6-4436-4e9f-8af0-228135d53207.png)

The *Patient_information* will be filtered for *Patien ID*.

![image](https://user-images.githubusercontent.com/115709957/209002330-ceaac104-64a6-4fb4-8025-a9b4419b6302.png)

The email will be send to the email address stored in the Sheet *Patient_Information*

![image](https://user-images.githubusercontent.com/115709957/209002360-65598a09-50a1-4b75-a5f1-10baf58fe8ed.png)

In case the decision table would find a drug interaction the output will be red. After the pharmacist double checks and verifies the drug interaction an email will be send directly to the physicion to inform him about the issue. Therefore we implemented the third make scenario (*Pharmacy_Scenario3_DrugInteractionDetected.json*) which will send a email back to the physician.

![image](https://user-images.githubusercontent.com/115709957/209002385-4b92bf3b-acb7-483f-a98e-954e7e492c37.png)

The data of the responsible physcician is stored in the *google form* and the google sheet *Physician_information* stores their email address.

![image](https://user-images.githubusercontent.com/115709957/209002424-8511c387-5e7f-4958-8cf5-022ce60b3e63.png)

The email will be send and the physician is able to handle the issue immediately. 


![image](https://user-images.githubusercontent.com/115709957/209002467-5975762b-d168-4992-83c0-d7e3c0096ed0.png)

And then the Email will be sent to the Physician.

## Fully automated Process

As you can see we were also able to make the whole process fully automated. When the prescription is filled and Pharmacy B is chosen, the process will be triggered and an email will be sent to the patient or doctor depending on the outcome of the drug interaction check (the decision table).

![image](https://user-images.githubusercontent.com/114395669/209151256-d6867e3d-9fa7-4e32-953a-a4d366f78a7a.png)

![image](https://user-images.githubusercontent.com/115709957/209134589-682562cd-88ca-4f8e-8518-6527c1318c0b.png)


Please note that we have two business process models uploaded. One has Pharmacy A semi automated and Pharmacy B only with user tasks. Once we got Pharmacy A semi automated, we fully automated Pharmacy B and uploaded a new business process model. We are fully aware that this can be done in the same model. However, this is for purpose of demonstration as we did not want it to interfere with the make scenario we have already created for the semi automated Pharmacy A.






