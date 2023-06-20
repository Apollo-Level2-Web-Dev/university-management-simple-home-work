# Practice Task: Complete Faculty (As a User) Module 

Do not forget to add routes in `routes/index.ts` file.

### Create routes, controllers ,services,constants,validation , utils for  the admin module  given below

#### Root route should be `api/v1/users`.

```typescript
router.post(
  '/create-faculty',
  validateRequest(FacultyController.createFacultyZodSchema),
  FacultyController.createFaculty)
);
```
### Things to do

- Generate a utility function to create faculty incremental id. Pattern `F-00001`

#### Root route should be `api/v1/faculties`.

```typescript
router.get('/',FacultyController.getAllFaculties);

router.get('/:id', FacultyController.getSingleFaculty);

router.patch('/:id', 
  validateRequest( FacultyController.updateFacultyZodSchema),
  FacultyController.updateFaculty
);
```


### Faculty
- _id: ObjectID
-  id: string;
-  name:
    -  firstName
    -  middleName (optional)
    -  lastName
-  dateOfBirth
-  email
-  contactNo
-  emergencyContactNo
-  gender
-  permanentAddress  
-  presentAddress
-  bloodGroup (optional)
-  designation
-  academicDepartment ( reference )
-  academicFaculty ( reference )
-  profileImage (optional)
-  createdAt


#### Sample Data

```json
{
  "_id":ObjectId("6425c04cc4edab97a3ebc749")
  "id": "F-00002",
  "name": {
    "firstName": "Mezbaul ",
    "lastName": "Persian",
    "middleName": "Abedin"
  },
  "dateOfBirth": "24-04-1998",
  "gender": "male",
  "bloodGroup": "O+",
  "email": "mezbaul@gmail.com",
  "contactNo": "01800000006",
  "emergencyContactNo": "01800000006",
  "presentAddress": "ctg",
  "permanentAddress": "ctg",
  "designation": "Lecturer",
  "academicDepartment":"6429e7d524d69a1815cc37f7",
  "academicFaculty":"6429f04b3c14b1f9a7c2d97a",
  "profileImage": "https://via.placeholder.com/150x150",
  "createdAt": "2023-05-31T14:42:22.747Z",
  "updatedAt": "2023-06-01T08:54:57.058Z"
}
```


#### Sample Data (After Populate)

```json
{
  "_id":ObjectId("6425c04cc4edab97a3ebc749")
  "id": "F-00002",
  "name": {
    "firstName": "Mezbaul ",
    "lastName": "Persian",
    "middleName": "Abedin"
  },
  "dateOfBirth": "24-04-1998",
  "gender": "male",
  "bloodGroup": "O+",
  "email": "mezbaul@gmail.com",
  "contactNo": "01800000006",
  "emergencyContactNo": "01800000006",
  "presentAddress": "ctg",
  "permanentAddress": "ctg",
  "designation": "Lecturer",
  "academicDepartment": {
    "_id": "6429e7d524d69a1815cc37f7",
    "title": "Department of Computer Science and Engineering",
    "createdAt": "2023-05-28T21:24:53.677Z",
    "updatedAt": "2023-05-28T21:24:53.677Z"
  },
  "academicFaculty": {
    "_id": "6429f04b3c14b1f9a7c2d97a",
    "title": "Faculty of Science and Engineering",
    "createdAt": "2023-05-28T21:24:53.677Z",
    "updatedAt": "2023-05-28T21:24:53.677Z"
  },
  "profileImage": "https://via.placeholder.com/150x150",
  "createdAt": "2023-05-31T14:42:22.747Z",
  "updatedAt": "2023-06-01T08:54:57.058Z"
}
```















