# ShrRestClient.DefaultApi

All URIs are relative to *http://localhost:3001/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPatientById**](DefaultApi.md#getPatientById) | **GET** /patient/{shrId} | Find patient by SHR ID
[**patientOptions**](DefaultApi.md#patientOptions) | **OPTIONS** /patient | 
[**updatePatientRecord**](DefaultApi.md#updatePatientRecord) | **PUT** /patient | Update a single patient record


<a name="getPatientById"></a>
# **getPatientById**
> getPatientById(shrId)

Find patient by SHR ID

Returns a single patient record

### Example
```javascript
var ShrRestClient = require('shr_rest_client');

var apiInstance = new ShrRestClient.DefaultApi();

var shrId = "shrId_example"; // String | ID of patient to return


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.getPatientById(shrId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shrId** | **String**| ID of patient to return | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

<a name="patientOptions"></a>
# **patientOptions**
> patientOptions()



### Example
```javascript
var ShrRestClient = require('shr_rest_client');

var apiInstance = new ShrRestClient.DefaultApi();

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.patientOptions(callback);
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="updatePatientRecord"></a>
# **updatePatientRecord**
> updatePatientRecord(patient)

Update a single patient record

Updates a single patient record

### Example
```javascript
var ShrRestClient = require('shr_rest_client');

var apiInstance = new ShrRestClient.DefaultApi();

var patient = [new ShrRestClient.[Object]()]; // [Object] | Patient object to update


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.updatePatientRecord(patient, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **patient** | **[Object]**| Patient object to update | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

