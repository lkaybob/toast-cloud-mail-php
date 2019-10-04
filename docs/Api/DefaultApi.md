# ToastCloud\DefaultApi

All URIs are relative to *https://api-mail.cloud.toast.com/email/v1.5/appKeys/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**appKeySenderEachMailPost**](DefaultApi.md#appKeySenderEachMailPost) | **POST** /{appKey}/sender/eachMail | 개별 메일 발송
[**appKeySenderMailsGet**](DefaultApi.md#appKeySenderMailsGet) | **GET** /{appKey}/sender/mails | 메일 발송 리스트 조회
[**sendMail**](DefaultApi.md#sendMail) | **POST** /{appKey}/sender/mail | 일반 메일 발송


# **appKeySenderEachMailPost**
> appKeySenderEachMailPost($appKey, $body)

개별 메일 발송

수신자 각각에게 메일을 보냄 (받는 사람에게 수신자는 한 명만)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new ToastCloud\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$appKey = "appKey_example"; // string | Project별 고유의 앱키
$body = new \ToastCloud\Model\MailBody(); // \ToastCloud\Model\MailBody | 

try {
    $apiInstance->appKeySenderEachMailPost($appKey, $body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->appKeySenderEachMailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appKey** | **string**| Project별 고유의 앱키 |
 **body** | [**\ToastCloud\Model\MailBody**](../Model/MailBody.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=UTF-8
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appKeySenderMailsGet**
> appKeySenderMailsGet($appKey, $requestId, $startSendDate, $endSendDate, $mailStatusCode)

메일 발송 리스트 조회

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new ToastCloud\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$appKey = "appKey_example"; // string | Project별 고유의 앱키
$requestId = "requestId_example"; // string | 요청 ID (조건적 필수 - 1)
$startSendDate = "startSendDate_example"; // string | 발송 시점 조회 시작값 (조건적 필수 - 2)
$endSendDate = "endSendDate_example"; // string | 발송 시점 조회 종료값 (조건적 필수 - 2)
$mailStatusCode = "mailStatusCode_example"; // string | 발송상태코드 (발송준비, 발송중, 발송완료, 발송실패 순)

try {
    $apiInstance->appKeySenderMailsGet($appKey, $requestId, $startSendDate, $endSendDate, $mailStatusCode);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->appKeySenderMailsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appKey** | **string**| Project별 고유의 앱키 |
 **requestId** | **string**| 요청 ID (조건적 필수 - 1) | [optional]
 **startSendDate** | **string**| 발송 시점 조회 시작값 (조건적 필수 - 2) | [optional]
 **endSendDate** | **string**| 발송 시점 조회 종료값 (조건적 필수 - 2) | [optional]
 **mailStatusCode** | **string**| 발송상태코드 (발송준비, 발송중, 발송완료, 발송실패 순) | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: appication/json;charset=UTF-8
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendMail**
> sendMail($appKey, $body)

일반 메일 발송

메일 발송시, 수신자 목록을 누구나 확인할 수 있음

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new ToastCloud\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$appKey = "appKey_example"; // string | Project별 고유의 앱키
$body = new \ToastCloud\Model\Receiver(); // \ToastCloud\Model\Receiver | 

try {
    $apiInstance->sendMail($appKey, $body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->sendMail: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appKey** | **string**| Project별 고유의 앱키 |
 **body** | [**\ToastCloud\Model\Receiver**](../Model/Receiver.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=UTF-8
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

