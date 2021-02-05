# Customer Import Platform MQA

### Assignment
A system that imports CSV files with certain parameters. After file import, a Customer entity is created with appropriate fields.
CSV file must contain the following mandatory values: first_name, last_name, email, date_of_birth
The system is available by: https://testtaskmatic.herokuapp.com

### Requirements
* Prepare test documentation (set of checklists/test cases) for the platform - define the sufficient number of test artirafacts, but don't overkill yourself with exhaustive coverage.   
* Test app with help of test documentation and find all possible defects. 
* Use Google Sheet for bugs and test cases (we will send you a link).
* Compose the brief execution report based on the test results and discovered issues (choose any preferable representation - excel, ppt, doc, etc.)

### Recommendations
Recommended duration for the test task is 3 days.
(Expected hourly duration is 6-8 hours)

You may use API requests for testing The platform has following API endpoints:

**Create import:**
```
POST /api/imports 
content-type: multipart/form-data 
import[file]=@list.csv 
import[title]=MyImport
```

**Start import:**
```
POST /api/imports/<import_id>/start
```

**Get import:**
```
GET /api/imports/<import_id>
```

**Update import:**
```
PUT /api/imports/<import_id>
content-type: multipart/form-data
import[title]=MyImport
```

**Get customers:**
```
GET /api/imports/<import_id>/customers
```

**Delete import:**
```
DELETE /api/imports/<import_id>
```

**Authorization Header:**
`Authorization: Bearer 1f43d455fgjkgfjgf48`

As you work on your solution you will inevitably have questions - please send all inquiries via slack. We are happy to assist and help
