# @datafire/amazonaws_api_pricing

Client library for AWS Price List Service

## Installation and Usage
```bash
npm install --save @datafire/amazonaws_api_pricing
```
```js
let amazonaws_api_pricing = require('@datafire/amazonaws_api_pricing').create({
  accessKeyId: "",
  secretAccessKey: "",
  region: ""
});

amazonaws_api_pricing.DescribeServices({}).then(data => {
  console.log(data);
});
```

## Description

<p>AWS Price List Service API (AWS Price List Service) is a centralized and convenient way to programmatically query Amazon Web Services for services, products, and pricing information. The AWS Price List Service uses standardized product attributes such as <code>Location</code>, <code>Storage Class</code>, and <code>Operating System</code>, and provides prices at the SKU level. You can use the AWS Price List Service to build cost control and scenario planning tools, reconcile billing data, forecast future spend for budgeting purposes, and provide cost benefit analysis that compare your internal workloads with AWS.</p> <p>Use <code>GetServices</code> without a service code to retrieve the service codes for all AWS services, then <code>GetServices</code> with a service code to retreive the attribute names for that service. After you have the service code and attribute names, you can use <code>GetAttributeValues</code> to see what values are available for an attribute. With the service code and an attribute name and value, you can use <code>GetProducts</code> to find specific products that you're interested in, such as an <code>AmazonEC2</code> instance, with a <code>Provisioned IOPS</code> <code>volumeType</code>.</p> <p>Service Endpoint</p> <p>AWS Price List Service API provides the following two endpoints:</p> <ul> <li> <p>https://api.pricing.us-east-1.amazonaws.com</p> </li> <li> <p>https://api.pricing.ap-south-1.amazonaws.com</p> </li> </ul>

## Actions

### DescribeServices



```js
amazonaws_api_pricing.DescribeServices({}, context)
```

#### Input
* input `object`
  * MaxResults `string`
  * NextToken `string`
  * FormatVersion [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode [String](#string)

#### Output
* output [DescribeServicesResponse](#describeservicesresponse)

### GetAttributeValues



```js
amazonaws_api_pricing.GetAttributeValues({
  "ServiceCode": "",
  "AttributeName": ""
}, context)
```

#### Input
* input `object`
  * MaxResults `string`
  * NextToken `string`
  * AttributeName **required** [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode **required** [String](#string)

#### Output
* output [GetAttributeValuesResponse](#getattributevaluesresponse)

### GetProducts



```js
amazonaws_api_pricing.GetProducts({}, context)
```

#### Input
* input `object`
  * MaxResults `string`
  * NextToken `string`
  * Filters [Filters](#filters)
  * FormatVersion [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode [String](#string)

#### Output
* output [GetProductsResponse](#getproductsresponse)



## Definitions

### AttributeNameList
* AttributeNameList `array`
  * items [String](#string)

### AttributeValue
* AttributeValue `object`: The values of a given attribute, such as <code>Throughput Optimized HDD</code> or <code>Provisioned IOPS</code> for the <code>Amazon EC2</code> <code>volumeType</code> attribute.
  * Value [String](#string)

### AttributeValueList
* AttributeValueList `array`
  * items [AttributeValue](#attributevalue)

### BoxedInteger
* BoxedInteger `integer`

### DescribeServicesRequest
* DescribeServicesRequest `object`
  * FormatVersion [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode [String](#string)

### DescribeServicesResponse
* DescribeServicesResponse `object`
  * FormatVersion [String](#string)
  * NextToken [String](#string)
  * Services [ServiceList](#servicelist)

### ExpiredNextTokenException
* ExpiredNextTokenException `object`: The pagination token expired. Try again without a pagination token.
  * Message [errorMessage](#errormessage)

### Filter
* Filter `object`: The constraints that you want all returned products to match.
  * Field **required** [String](#string)
  * Type **required** [FilterType](#filtertype)
  * Value **required** [String](#string)

### FilterType
* FilterType `string` (values: TERM_MATCH)

### Filters
* Filters `array`
  * items [Filter](#filter)

### GetAttributeValuesRequest
* GetAttributeValuesRequest `object`
  * AttributeName **required** [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode **required** [String](#string)

### GetAttributeValuesResponse
* GetAttributeValuesResponse `object`
  * AttributeValues [AttributeValueList](#attributevaluelist)
  * NextToken [String](#string)

### GetProductsRequest
* GetProductsRequest `object`
  * Filters [Filters](#filters)
  * FormatVersion [String](#string)
  * MaxResults [BoxedInteger](#boxedinteger)
  * NextToken [String](#string)
  * ServiceCode [String](#string)

### GetProductsResponse
* GetProductsResponse `object`
  * FormatVersion [String](#string)
  * NextToken [String](#string)
  * PriceList [PriceList](#pricelist)

### InternalErrorException
* InternalErrorException `object`: An error on the server occurred during the processing of your request. Try again later.
  * Message [errorMessage](#errormessage)

### InvalidNextTokenException
* InvalidNextTokenException `object`: The pagination token is invalid. Try again without a pagination token.
  * Message [errorMessage](#errormessage)

### InvalidParameterException
* InvalidParameterException `object`: One or more parameters had an invalid value.
  * Message [errorMessage](#errormessage)

### NotFoundException
* NotFoundException `object`: The requested resource can't be found.
  * Message [errorMessage](#errormessage)

### PriceList
* PriceList `array`
  * items [PriceListItemJSON](#pricelistitemjson)

### PriceListItemJSON
* PriceListItemJSON `string`

### Service
* Service `object`: The metadata for a service, such as the service code and available attribute names.
  * AttributeNames [AttributeNameList](#attributenamelist)
  * ServiceCode [String](#string)

### ServiceList
* ServiceList `array`
  * items [Service](#service)

### String
* String `string`

### errorMessage
* errorMessage `string`


