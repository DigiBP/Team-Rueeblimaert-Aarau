# Team-Rueeblimaert-Aarau
## Members

- Leena Anthony
- Aletta Karsies
- Paul Stehberger
- Andreas Heule

## Introduction

In Switzerland, drugs with medical promise are usually sold and handed over to the patient in pharmacies. Depending on the category of a drug a prescription by a medical doctor is needed.

In our project, we focus on the interaction between the medical doctor in a practice or hospital who fills the drug prescription and the pharmacy, as well as the process in the pharmacy where the prescription is checked and the required drug is eventually sold.

In today's common practice medical doctors and pharmacies both store the prescription information in their respective information systems which are **not** connected. Sending a prescription from a doctor's practice to the pharmacy is mostly done via email or on paper. In addition, there is no common database containing the patient's complete medication information.

## Our Goal

We want to digitalise the procedure and the handling of prescriptions and therefore gain more efficiency for pharmacies. One other positive effect is going to be the improvement of drug interaction checks for patients.  
The prescription will be sent to the pharmacy by filling out a Google form. The pharmacy receives the order and sees the current medication of the patient. With a decision table the medication will be checked for drug interaction. The pharmacist then double checks the data. After that, depending of the check result, the patient will be informed by email to kindly pick up their medication, or the prescribing physician will be informed about the detected drug interaction by email.

![image](https://user-images.githubusercontent.com/115709957/209010933-959bf8d1-bb6a-4d2a-9c92-da9564c3c892.png)


## List of Assumptions

- To simplify our project the patient can only choose from two pharmacies **A** and **B**
-	The used Google documents are secure and personal data will not leak
-	Our Google sheet has the same function as a database
- The decision table is simplified and would be replaced with a software approved by SwissMedic. We also do not distinguish between drug name and active ingredient

## Start of the Process:

In our digitalised process, the patient goes to a physician. If needed the medical doctor writes a prescription by filling out the [Google form][1] (ten questions). Our BPN process starts as soon as the physician sends the Google form. In the screenshots below is an example of our Google form.

[1]: https://docs.google.com/forms/d/e/1FAIpQLSfqVcNNJvv8UbSqdx3HZtLKWscjcq13AHXkysQsV_cB3ej1MA/viewform
![image](https://user-images.githubusercontent.com/115709957/209001835-aad677fd-aff0-4c5e-b1d3-844213653510.png)

By sending the Google form, a new row is automatically inserted in the [Prescription Form (Responses)][2].

[2]: https://docs.google.com/spreadsheets/d/1xP-jTlqB5-bax8qxv7f1s43OcnDquWo0AHF_OP_aLEc/edit#gid=1636714263

![image](https://user-images.githubusercontent.com/115709957/209001861-63387c09-e27e-40cc-b552-2ce6e6a32de7.png)

By choosing **Pharmacy A** or **Pharmacy B** in the google form. Our first make scenario (*Pharmacy_Scenario1_Task1.json*) will send the data to either **Pharmacy A** or **Pharmacy B**.

![image](https://user-images.githubusercontent.com/115709957/209001900-3ed89301-9fc3-4b4d-b506-2e13b30b0221.png)

The Router will filter the data for Pharamacy A or B and then pass it along to the right Pharmacy

![image](https://user-images.githubusercontent.com/115709957/209001948-df0d4acf-8b5d-46f6-8c3e-5b05f61759f6.png)
All Data will be passed to pharmacy A. 

![image](https://user-images.githubusercontent.com/115709957/209001997-b57b0000-bd0c-4d2b-b819-7fd4b736b58a.png)
Then the data will be send back to comunda and the process is initiated in Pharmacy A

![image](https://user-images.githubusercontent.com/115709957/209002024-025f681d-5645-4485-a107-7f8cfc40dd92.png)

![image](https://user-images.githubusercontent.com/115709957/209002041-92716fb0-dc5d-430e-b7d2-db0b8903b8c5.png)

google sheet
![image](https://user-images.githubusercontent.com/115709957/209002059-38188e99-f47c-4e14-ac19-efb56850bdd4.png)

1.tool
![image](https://user-images.githubusercontent.com/115709957/209002076-fc30e509-9adb-4b1e-ab24-cd61765b9696.png)

2. tool
![image](https://user-images.githubusercontent.com/115709957/209002155-d18210f1-840d-4e09-9697-6f8a545e9f7b.png)

http: the medication record then will be send back to comunda
![image](https://user-images.githubusercontent.com/115709957/209002192-fe4cd3e0-738c-46a9-b9e3-8fbf42a5b78a.png)

![image](https://user-images.githubusercontent.com/115709957/209002225-e2b43dcd-a031-4c59-9288-9dfc32a36c2b.png)

![image](https://user-images.githubusercontent.com/115709957/209002242-8df6160b-c570-4697-97d2-37efae24cec4.png)


![image](https://user-images.githubusercontent.com/115709957/209002255-6a2446d5-12c5-4b01-95ff-35bec9754c67.png)

![image](https://user-images.githubusercontent.com/115709957/209002279-2509f8f1-d1c8-477c-9d0b-bfaa34a3603c.png)

![image](https://user-images.githubusercontent.com/115709957/209002298-86c4577a-ed93-4a6d-9398-390e52d3bfc4.png)
User task: Medication will be prepared to pick up. When its ready. Emali will be send

![image](https://user-images.githubusercontent.com/115709957/209002318-0fa33eb6-4436-4e9f-8af0-228135d53207.png)

![image](https://user-images.githubusercontent.com/115709957/209002330-ceaac104-64a6-4fb4-8025-a9b4419b6302.png)


Email
![image](https://user-images.githubusercontent.com/115709957/209002360-65598a09-50a1-4b75-a5f1-10baf58fe8ed.png)

![image](https://user-images.githubusercontent.com/115709957/209002385-4b92bf3b-acb7-483f-a98e-954e7e492c37.png)


Google sheet
![image](https://user-images.githubusercontent.com/115709957/209002424-8511c387-5e7f-4958-8cf5-022ce60b3e63.png)


Email
![image](https://user-images.githubusercontent.com/115709957/209002467-5975762b-d168-4992-83c0-d7e3c0096ed0.png)
And then the Email will be send to the Physician










