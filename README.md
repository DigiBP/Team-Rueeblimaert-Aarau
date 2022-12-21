# Team-Rueeblimaert-Aarau
## Members

- Leena Anthony
- Aletta Karsies
- Paul Stehberger
- Andreas Heule

## Introduction

In Switzerland, drugs with medical promise are usually sold and handed over to the patient in pharmacies. Depending on the category of a drug a prescription by a medical doctor is needed.

In our project, we focus on the interaction between the medical doctor in a practice or hospital who fills the drug prescription and the pharmacy. As well as the process in the pharmacy where the prescription is checked and the required drug is eventually sold.

In today's common practice medical doctors and pharmacies both store the prescription information in their respective information systems which are **not** connected. Sending a prescription from a doctor's practice to the pharmacy is mostly done via email or on paper. In addition, there is no common database containing the patient's complete medication information.

## Our Goal

We want to digitalise the procedure and the handling of prescriptions and therefore gain more efficiency for pharmacies. One other positive effect is going to be the improvement of drug interaction checks for patients.  
The prescription will be sent to the pharmacy by filling out a Google form. The pharmacy receives the order and sees the current medication of the patient. With a decision table the medication will be checked for drug interaction. The pharmacist then double checks the data. After that the patient will be informed by email to kindly pick up their medication.

## List of Assumptions

- To simplify our project the patient can only choose from two pharmacies **A** and **B**
-	The used Google documents are secure and personal data will not leak
-	Our Google sheet has the same function as a database
- The decision table is simplyfied and would be replaced with a software approved by SwissMedic

## Start of the Process:

In our digitalised process, the patient goes to a physician. If needed the medical doctor writes a prescription by filling out the [Google form][1] (ten questions). Our BPN process starts as soon as the physician sends the Google form. In the screenshots below is an example of our Google form.

[1]: https://docs.google.com/forms/d/e/1FAIpQLSfqVcNNJvv8UbSqdx3HZtLKWscjcq13AHXkysQsV_cB3ej1MA/viewform
![Google_Form_Bild](https://user-images.githubusercontent.com/115709957/208297194-c8e7322f-9d16-46d3-89f3-b84006da64dc.jpg)

By sending the Google form, a new row is automatically inserted in the [Prescription Form (Responses)][2].

[2]: https://docs.google.com/spreadsheets/d/1xP-jTlqB5-bax8qxv7f1s43OcnDquWo0AHF_OP_aLEc/edit#gid=1636714263

![image](https://user-images.githubusercontent.com/115709957/208297491-2eea2048-43d4-4e56-98b9-06a952f9f7c6.png)

By choosing **Pharmacy A** and sending the Google form. The process is then automatically initiated in *Pharmacy A*.
![image](https://user-images.githubusercontent.com/115709957/208297748-970dff39-1174-448f-b9ab-a80520d03fdb.png)

As you can see the process is initiated in *Pharmacy A*.
![image](https://user-images.githubusercontent.com/115709957/208297768-95fd1ed4-f18a-41af-ad33-e077509ad49f.png)



![image](https://user-images.githubusercontent.com/115709957/209003206-a2c82dd7-a49b-406f-a818-1caccd0432b6.png)



![image](https://user-images.githubusercontent.com/115709957/209003223-7b4bb595-100c-4a7f-a66c-5aa1fc6cfc8e.png)


![image](https://user-images.githubusercontent.com/115709957/209003239-8c7be2d8-7dfb-4e68-8652-d951d1c79300.png)

By choosing **Pharmacy A** or **Pharmacy B** in the google form. Our first make scenario (*Pharmacy_Scenario1_Task1.json*) will send the data to either **Pharmacy A** or **Pharmacy B**.

![image](https://user-images.githubusercontent.com/115709957/209003259-4c3ad0c3-78af-430b-b385-4afe6a544a97.png)

The Router will filter the data for Pharamacy A or B and then pass it along to the right Pharmacy

![image](https://user-images.githubusercontent.com/115709957/209003306-e99a6839-a217-4556-88fc-c59c3f4915c6.png)

All Data will be passed to pharmacy A. 
![image](https://user-images.githubusercontent.com/115709957/209003336-c59e9b30-929a-46e0-a1f0-53debdb87e61.png)

Then the data will be send back to comunda and the process is initiated in Pharmacy A

![image](https://user-images.githubusercontent.com/115709957/209003376-05788366-7c03-4ec4-854a-527e3de9cf6b.png)

![image](https://user-images.githubusercontent.com/115709957/209003386-66261f66-a2e4-4b54-89f9-53c45516918a.png)

Google sheets
![image](https://user-images.githubusercontent.com/115709957/209003423-8a47b17a-5d3c-411c-8ba9-6e6cc2afdd52.png)


1. tool
![image](https://user-images.githubusercontent.com/115709957/209003475-8a2759d1-0bd2-49e4-ae91-744d5bf74693.png)

2. Tool
![image](https://user-images.githubusercontent.com/115709957/209003510-6a385fd3-79a9-4120-84e2-32f0d3f19786.png)

http: the medication record then will be send back to comunda
![image](https://user-images.githubusercontent.com/115709957/209003530-e29838ab-ec55-4a1d-b066-7c429e51f23c.png)

![image](https://user-images.githubusercontent.com/115709957/209003542-fdbc5279-cc0e-4bad-8d68-87f07998f7a2.png)


![image](https://user-images.githubusercontent.com/115709957/209003554-925acea7-487e-4df7-a340-9aea86ec2dec.png)

![image](https://user-images.githubusercontent.com/115709957/209003571-572edce4-0a9a-4894-9da0-3352c845cc5e.png)

![image](https://user-images.githubusercontent.com/115709957/209003582-29b31f48-6545-4700-8c5b-0906f6efbef0.png)

![image](https://user-images.githubusercontent.com/115709957/209003595-87faecf9-eed2-4230-8b31-bff948f87fc4.png)

User task: Medication will be prepared to pick up. When its ready. Emali will be send

![image](https://user-images.githubusercontent.com/115709957/209003641-8d371ab1-528b-4701-a909-c5f9c9216c58.png)

Google sheets
![image](https://user-images.githubusercontent.com/115709957/209003675-4038a51d-358b-4fff-9bdb-ec89a0bb8779.png)

Email
![image](https://user-images.githubusercontent.com/115709957/209003705-4d7c7cc8-f6a6-4b92-a590-99ee83097021.png)


![image](https://user-images.githubusercontent.com/115709957/209004203-b05290a4-ffd7-4383-9a4b-eb7397cd020e.png)


![image](https://user-images.githubusercontent.com/115709957/209003719-dc567939-506b-44b7-b833-99df3a4cdf60.png)


Google sheet
![image](https://user-images.githubusercontent.com/115709957/209004230-a3034bee-5209-458e-9b55-ca1d8420cb29.png)


Email

![image](https://user-images.githubusercontent.com/115709957/209004255-20a5d5a1-792e-4341-811b-0a6c71925342.png)

And then the Email will be send to the Physician
































