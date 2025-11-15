# cloudmersive-documentai-api-client

CloudmersiveDocumentaiApiClient - JavaScript client for cloudmersive-documentai-api-client
Use next-generation AI to extract data, fields, insights and text from documents. Instantly.
[Cloudmersive Document AI API](https://cloudmersive.com/document-ai-api) provides advanced data extraction from documents.

- API version: v1
- Package version: 1.3.1


## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install cloudmersive-documentai-api-client --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your cloudmersive-documentai-api-client from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('cloudmersive-documentai-api-client')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var CloudmersiveDocumentaiApiClient = require('cloudmersive-documentai-api-client');

var defaultClient = CloudmersiveDocumentaiApiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix['Apikey'] = "Token"

var api = new CloudmersiveDocumentaiApiClient.AnalyzeApi()

var opts = { 
  'body': new CloudmersiveDocumentaiApiClient.DocumentPolicyRequest() // {DocumentPolicyRequest} Input request, including document and policy rules
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.applyRules(opts, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CloudmersiveDocumentaiApiClient.AnalyzeApi* | [**applyRules**](docs/AnalyzeApi.md#applyRules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractAllFieldsAndTables**](docs/ExtractApi.md#extractAllFieldsAndTables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractBarcodes**](docs/ExtractApi.md#extractBarcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractClassification**](docs/ExtractApi.md#extractClassification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractClassificationAdvanced**](docs/ExtractApi.md#extractClassificationAdvanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractFields**](docs/ExtractApi.md#extractFields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractFieldsAdvanced**](docs/ExtractApi.md#extractFieldsAdvanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractSummary**](docs/ExtractApi.md#extractSummary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractTables**](docs/ExtractApi.md#extractTables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
*CloudmersiveDocumentaiApiClient.ExtractApi* | [**extractText**](docs/ExtractApi.md#extractText) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI
*CloudmersiveDocumentaiApiClient.RunBatchJobApi* | [**extractAllFieldsAndTablesFromDocumentBatchJob**](docs/RunBatchJobApi.md#extractAllFieldsAndTablesFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
*CloudmersiveDocumentaiApiClient.RunBatchJobApi* | [**extractClassificationFromDocumentBatchJob**](docs/RunBatchJobApi.md#extractClassificationFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
*CloudmersiveDocumentaiApiClient.RunBatchJobApi* | [**extractFieldsFromDocumentAdvancedBatchJob**](docs/RunBatchJobApi.md#extractFieldsFromDocumentAdvancedBatchJob) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
*CloudmersiveDocumentaiApiClient.RunBatchJobApi* | [**extractTextFromDocumentBatchJob**](docs/RunBatchJobApi.md#extractTextFromDocumentBatchJob) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
*CloudmersiveDocumentaiApiClient.RunBatchJobApi* | [**getAsyncJobStatus**](docs/RunBatchJobApi.md#getAsyncJobStatus) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


## Documentation for Models

 - [CloudmersiveDocumentaiApiClient.AdvancedExtractClassificationRequest](docs/AdvancedExtractClassificationRequest.md)
 - [CloudmersiveDocumentaiApiClient.AdvancedExtractFieldsRequest](docs/AdvancedExtractFieldsRequest.md)
 - [CloudmersiveDocumentaiApiClient.DocumentAdvancedClassificationResult](docs/DocumentAdvancedClassificationResult.md)
 - [CloudmersiveDocumentaiApiClient.DocumentCategories](docs/DocumentCategories.md)
 - [CloudmersiveDocumentaiApiClient.DocumentClassificationResult](docs/DocumentClassificationResult.md)
 - [CloudmersiveDocumentaiApiClient.DocumentPolicyRequest](docs/DocumentPolicyRequest.md)
 - [CloudmersiveDocumentaiApiClient.DocumentPolicyResult](docs/DocumentPolicyResult.md)
 - [CloudmersiveDocumentaiApiClient.ExtractBarcodesAiResponse](docs/ExtractBarcodesAiResponse.md)
 - [CloudmersiveDocumentaiApiClient.ExtractDocumentBatchJobResult](docs/ExtractDocumentBatchJobResult.md)
 - [CloudmersiveDocumentaiApiClient.ExtractDocumentJobStatusResult](docs/ExtractDocumentJobStatusResult.md)
 - [CloudmersiveDocumentaiApiClient.ExtractFieldsAndTablesResponse](docs/ExtractFieldsAndTablesResponse.md)
 - [CloudmersiveDocumentaiApiClient.ExtractFieldsResponse](docs/ExtractFieldsResponse.md)
 - [CloudmersiveDocumentaiApiClient.ExtractTablesResponse](docs/ExtractTablesResponse.md)
 - [CloudmersiveDocumentaiApiClient.ExtractTextResponse](docs/ExtractTextResponse.md)
 - [CloudmersiveDocumentaiApiClient.ExtractedBarcodeItem](docs/ExtractedBarcodeItem.md)
 - [CloudmersiveDocumentaiApiClient.ExtractedTextPage](docs/ExtractedTextPage.md)
 - [CloudmersiveDocumentaiApiClient.FieldToExtract](docs/FieldToExtract.md)
 - [CloudmersiveDocumentaiApiClient.FieldValue](docs/FieldValue.md)
 - [CloudmersiveDocumentaiApiClient.PolicyRule](docs/PolicyRule.md)
 - [CloudmersiveDocumentaiApiClient.PolicyRuleViolation](docs/PolicyRuleViolation.md)
 - [CloudmersiveDocumentaiApiClient.SummarizeDocumentResponse](docs/SummarizeDocumentResponse.md)
 - [CloudmersiveDocumentaiApiClient.TableResult](docs/TableResult.md)
 - [CloudmersiveDocumentaiApiClient.TableResultCell](docs/TableResultCell.md)
 - [CloudmersiveDocumentaiApiClient.TableResultRow](docs/TableResultRow.md)


## Documentation for Authorization


### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

