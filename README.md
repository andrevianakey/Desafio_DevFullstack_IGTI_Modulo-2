# Module 2 Challenge - Bootcamp IGTI

Creation of API's with Node.js and Express.js from the Bootcamp Fullstack Developer IGTI.

The API provides endpoints for handling the grades.json file available in src / app / datasets.

The endpoints are:

- index
- show
- create
- update
- destroy
- sum
- average
- top3
you need to install the following dependencies:
- express
-
Insomnia workspace file with pre-configured requests. The file is located at the root of the project under the name insomnia.json.

Script:
Develop an API called “grades-control-api” to control student grades in course materials.

The challenge is to develop an API called “grades-control-api” to control student grades in course materials. Develop endpoints for creating, updating, deleting and querying notes, here called grids. The grids should be saved in a json file, called “grades.json”. This file will be previously provided and its endpoints must act considering the existing records.
A grid should have the fields below:
- id (int): unique identifier of the grid. It should be generated automatically by the API, and guaranteed that it will not be repeated.
- student (string): student's name. Example: “Guilherme Assis”. - subject (string): name of the subject. Example: “Mathematics”.
 
 - type (string): name of the activity. Example: “Final exam”. - value (float): grade of the activity. Example: 10.
- timestamp (string): launch time. Example: 2020-05-19T18: 21: 24.964Z. Tip: use JavaScript's “new Date ()”.
The grades.json file will be previously supplied with some inserted records, its endpoints should work considering their existence, and should not create a clean file for use. The file structure is as follows:
The nextId property should always store the next id that will be used when creating a new grid. The grids property has an array with several grids, each being represented by an object with the fields described previously.
You should develop the endpoints described below:
1. Create an endpoint to create a grid. This endpoint should receive as parameters the student, subject, type and value fields as described above. This grid must be saved in the json grades.json file, and must have a unique id associated with it. In the timestamp field, the date and time of the insertion time should be saved. The endpoint should return the grid object that was created. The API must guarantee the automatic increment of this identifier, so that it is not repeated between records. Within the grades.json file that was provided for use in the challenge, the nextId field already has a defined value. After insertion, this nextId must be incremented and saved in the file itself, so that the next insertion can be used.
   
 2. Create an endpoint to update a grid. This endpoint should receive as parameters the grid id to be changed and the student, subject, type and value fields. The endpoint must validate if the informed grid exists, if it does not exist, it should return an error. If it exists, the endpoint should update the information received by parameters in the registry, and update it with the new data changed in the grades.json file.
3. Create an endpoint to delete a grid. This endpoint should receive the grid id as a parameter and exclude it from the grades.json file.
4. Create an endpoint to query a specific grid. This endpoint should receive the grid id as a parameter and return its information.
5. Create an endpoint to see a student's total grade in a discipline. The endpoint must receive as a parameter the student and the subject, and perform the sum of all the activity notes corresponding to that subject for that student. The endpoint should return the sum of the value property of the records found.
6. Create an endpoint to see the average of the grids of a given subject and type. The endpoint must receive as a parameter a subject and a type, and return the average. The average is calculated by adding the value record of all records that have the subject and type informed, and dividing by the total number of records that have this same subject and type.
7. Create an endpoint to return the top three grids according to a given subject and type. The endpoint must receive as a parameter a subject and a type return an array with the three highest value records of that subject and type. The order must be from highest to lowest.
 Once finished, you can test the features using Insomnia, available at:  https://insomnia.rest/download/
  
 Insomnia is a free cross-platform desktop application that takes the pain out of interacting with HTTP-based APIs. Insomnia combines an easy-to-use interface with advanced functionality like authentication helpers, code generation, and environment variables. There is also the option to subscribe to a paid plan to gain access to encrypted data sync and team collaboration.
