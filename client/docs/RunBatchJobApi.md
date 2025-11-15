# CloudmersiveDocumentaiapiClient.RunBatchJobApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extractAllFieldsAndTablesFromDocumentBatchJob**](RunBatchJobApi.md#extractAllFieldsAndTablesFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
[**extractClassificationFromDocumentBatchJob**](RunBatchJobApi.md#extractClassificationFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
[**extractFieldsFromDocumentAdvancedBatchJob**](RunBatchJobApi.md#extractFieldsFromDocumentAdvancedBatchJob) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
[**extractTextFromDocumentBatchJob**](RunBatchJobApi.md#extractTextFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
[**getAsyncJobStatus**](RunBatchJobApi.md#getAsyncJobStatus) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


<a name="extractAllFieldsAndTablesFromDocumentBatchJob"></a>
# **extractAllFieldsAndTablesFromDocumentBatchJob**
> ExtractDocumentBatchJobResult extractAllFieldsAndTablesFromDocumentBatchJob(opts)

Extract All Fields and Tables of Data from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.RunBatchJobApi();

var opts = { 
  'recognitionMode': "recognitionMode_example", // String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  'inputFile': "/path/to/file.txt" // File | Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.extractAllFieldsAndTablesFromDocumentBatchJob(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

<a name="extractClassificationFromDocumentBatchJob"></a>
# **extractClassificationFromDocumentBatchJob**
> ExtractDocumentBatchJobResult extractClassificationFromDocumentBatchJob(opts)

Extract Classification or Category from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.RunBatchJobApi();

var opts = { 
  'categories': "categories_example", // String | Desired classification to extract
  'recognitionMode': "recognitionMode_example", // String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  'inputFile': "/path/to/file.txt" // File | Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.extractClassificationFromDocumentBatchJob(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **String**| Desired classification to extract | [optional] 
 **recognitionMode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

<a name="extractFieldsFromDocumentAdvancedBatchJob"></a>
# **extractFieldsFromDocumentAdvancedBatchJob**
> ExtractDocumentBatchJobResult extractFieldsFromDocumentAdvancedBatchJob(opts)

Extract Field Values from a Document using Advanced AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.RunBatchJobApi();

var opts = { 
  'recognitionMode': "recognitionMode_example", // String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  'body': new CloudmersiveDocumentaiapiClient.AdvancedExtractFieldsRequest() // AdvancedExtractFieldsRequest | 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.extractFieldsFromDocumentAdvancedBatchJob(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)|  | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

<a name="extractTextFromDocumentBatchJob"></a>
# **extractTextFromDocumentBatchJob**
> ExtractDocumentBatchJobResult extractTextFromDocumentBatchJob(opts)

Extract Text from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Input document formats supported include DOCX, PDF, PNG and JPG.  Supports a wide range of languages.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.RunBatchJobApi();

var opts = { 
  'recognitionMode': "recognitionMode_example", // String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  'inputFile': "/path/to/file.txt" // File | Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.extractTextFromDocumentBatchJob(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

<a name="getAsyncJobStatus"></a>
# **getAsyncJobStatus**
> ExtractDocumentJobStatusResult getAsyncJobStatus(opts)

Get the status and result of an Extract Document Batch Job

Returns the result of the Async Job - possible states can be STARTED or COMPLETED.  This API is only available for Cloudmersive Managed Instance and Private Cloud deployments.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.RunBatchJobApi();

var opts = { 
  'asyncJobID': "asyncJobID_example" // String | 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getAsyncJobStatus(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asyncJobID** | **String**|  | [optional] 

### Return type

[**ExtractDocumentJobStatusResult**](ExtractDocumentJobStatusResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

