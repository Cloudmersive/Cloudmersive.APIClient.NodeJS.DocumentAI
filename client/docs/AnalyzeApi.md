# CloudmersiveDocumentaiapiClient.AnalyzeApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyRules**](AnalyzeApi.md#applyRules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI


<a name="applyRules"></a>
# **applyRules**
> DocumentPolicyResult applyRules(opts)

Enforce Policies to a Document to allow or block it using Advanced AI

Enforce Policies to a Document to allow or block it using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```javascript
var CloudmersiveDocumentaiapiClient = require('cloudmersive-documentaiapi-client');
var defaultClient = CloudmersiveDocumentaiapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveDocumentaiapiClient.AnalyzeApi();

var opts = { 
  'body': new CloudmersiveDocumentaiapiClient.DocumentPolicyRequest() // DocumentPolicyRequest | Input request, including document and policy rules
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.applyRules(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DocumentPolicyRequest**](DocumentPolicyRequest.md)| Input request, including document and policy rules | [optional] 

### Return type

[**DocumentPolicyResult**](DocumentPolicyResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

