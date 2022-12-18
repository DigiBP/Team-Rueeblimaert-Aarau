# Team-Rueeblimaert-Aarau

## Introduction

In Switzerland, drugs with medical promise are usually sold and handed over to the patient in pharmacies. Depending on the category of a drug a prescription by a medical doctor is needed.

In our project, we focus on the interaction between the medical doctor in a practice or hospital who fills the drug prescription and the pharmacy. As well as the process in the pharmacy where the prescription is checked and the required drug is eventually sold.

In today's common practice medical doctors and pharmacies both store the prescription information in their respective information systems which are **not** connected. Sending a prescription from a doctor's practice to the pharmacy is mostly done via email or on paper. In addition, there is no common database containing the patient's complete medication information.

In order to digitalise and improve this process, we implemented a common database in which a pharmacist can view the summary of a certain patient including a newly added prescription. At the same time, viewing this information allows to check reliably for eventual drug interactions.

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


PICTURE MAKE CHECK DRUG INTERACTION / Filter for AHV Number

Explanation ….

PICTURE of the Process where the process waits at CHECK DRUG INTERACTION

Explanation 

Now the pharmacy sees the medication history of the patient (Picture). With the decision table (Picture) the patient's current medication intake is checked for drug interactions. The pharmacist double checks and the order is processed. 
