# TodolistApi

All URIs are relative to *https://{environment}.yukinari.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolistGet**](TodolistApi.md#todolistGet) | **GET** /todolist | Get all todolist
[**todolistPost**](TodolistApi.md#todolistPost) | **POST** /todolist | Create new todolist
[**todolistTodolistIdDelete**](TodolistApi.md#todolistTodolistIdDelete) | **DELETE** /todolist/{todolistId} | Delete existing todolist
[**todolistTodolistIdPut**](TodolistApi.md#todolistTodolistIdPut) | **PUT** /todolist/{todolistId} | Update existing todolist

<a name="todolistGet"></a>
# **todolistGet**
> ArrayTodolist todolistGet(includeDone, name)

Get all todolist

Get all active todolist by default

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
Boolean includeDone = false; // Boolean | Is include done todolist
String name = "name_example"; // String | Filter todolist by name
try {
    ArrayTodolist result = apiInstance.todolistGet(includeDone, name);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **includeDone** | **Boolean**| Is include done todolist | [optional] [default to false]
 **name** | **String**| Filter todolist by name | [optional]

### Return type

[**ArrayTodolist**](ArrayTodolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todolistPost"></a>
# **todolistPost**
> Todolist todolistPost(body)

Create new todolist

Create new todolist to database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
CreateOrUpdateTodolist body = new CreateOrUpdateTodolist(); // CreateOrUpdateTodolist | 
try {
    Todolist result = apiInstance.todolistPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateOrUpdateTodolist**](CreateOrUpdateTodolist.md)|  |

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="todolistTodolistIdDelete"></a>
# **todolistTodolistIdDelete**
> InlineResponse200 todolistTodolistIdDelete(todolistId)

Delete existing todolist

Delete existing todolist in database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
String todolistId = "todolistId_example"; // String | Todolist id for updated
try {
    InlineResponse200 result = apiInstance.todolistTodolistIdDelete(todolistId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistTodolistIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolistId** | **String**| Todolist id for updated |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todolistTodolistIdPut"></a>
# **todolistTodolistIdPut**
> Todolist todolistTodolistIdPut(body, todolistId)

Update existing todolist

Update existing todolist in database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
CreateOrUpdateTodolist body = new CreateOrUpdateTodolist(); // CreateOrUpdateTodolist | 
String todolistId = "todolistId_example"; // String | Todolist id for updated
try {
    Todolist result = apiInstance.todolistTodolistIdPut(body, todolistId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistTodolistIdPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateOrUpdateTodolist**](CreateOrUpdateTodolist.md)|  |
 **todolistId** | **String**| Todolist id for updated |

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

