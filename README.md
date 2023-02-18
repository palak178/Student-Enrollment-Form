# Student-Enrollment-Form
This repository contains the code for a simple web application that allows students to enroll in a course and stores the information in a JsonPowerDB database.

# Benefits of using JsonPowerDB
* Simple and easy to use web interface for student enrollment
* JsonPowerDB used as a high-performance NoSQL database for storing the student data
* Fast data retrieval and query capabilities provided by JsonPowerDB

# Technologies Used
* HTML
* CSS
* JAVASCRIPT
* JsonPowerDB ( As Database)

# Illustrations:
* UPDATE : when student roll number is already present in database then student information is fetched from database and filled in respective feild then user can UPDATE student information
* SAVE : If student roll number is not existed in database then we can fill other field and save in database
* clear : By this we can clear all field of form and with this except first field (roll-no) other field are disabled until user enter any roll number
* Alert : This website uses disposable Alter prompt using bootstrap

# Release History
**JsonPowerDB**
Version: 2.0

**Execute API**

```

var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}

```

**Create a PUT Request String**

```
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}
```

# Screenshots
