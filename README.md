# edgraph-platform-client

All Api- v1.0


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/EdGraph-OSS/php-sdk.git"
    }
  ],
  "require": {
    "EdGraph-OSS/php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/edgraph-platform-client/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$identityApiApiClientV1CreateApiClientRequest = new \EdGraph\PlatformClient\Model\IdentityApiApiClientV1CreateApiClientRequest(); // \EdGraph\PlatformClient\Model\IdentityApiApiClientV1CreateApiClientRequest | 

try {
    $result = $apiInstance->createTenantApiClientAsync($tenantId, $identityApiApiClientV1CreateApiClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->createTenantApiClientAsync: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.dev.edgraph.com/tenant*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIClientsApi* | [**createTenantApiClientAsync**](docs/Api/APIClientsApi.md#createtenantapiclientasync) | **POST** /tenants/{tenantId}/apiclients | Creates a new OpenId API Client
*APIClientsApi* | [**deleteTenantApiClientAsync**](docs/Api/APIClientsApi.md#deletetenantapiclientasync) | **DELETE** /tenants/{tenantId}/apiclients/{clientId} | Deletes an OpenId API Client
*APIClientsApi* | [**getAllTenantApiClientsAsync**](docs/Api/APIClientsApi.md#getalltenantapiclientsasync) | **GET** /tenants/{tenantId}/apiclients | Retrieves a list of OpenId API Clients associated to this tenant
*APIClientsApi* | [**getTenantApiClientByIdAsync**](docs/Api/APIClientsApi.md#gettenantapiclientbyidasync) | **GET** /tenants/{tenantId}/apiclients/{clientId} | Retrieves an OpenId API Client
*APIClientsApi* | [**regenerateTenantApiClientSecretAsync**](docs/Api/APIClientsApi.md#regeneratetenantapiclientsecretasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId}/regeneratesecret | Regenerates an OpenId API Client&#39;s secret
*APIClientsApi* | [**updateTenantApiClientAsync**](docs/Api/APIClientsApi.md#updatetenantapiclientasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId} | Updates an OpenId API Client
*AnalyticsConnectorsApi* | [**createConnector**](docs/Api/AnalyticsConnectorsApi.md#createconnector) | **POST** /tenants/{tenantId}/analytics/connectors | Creates a new connector
*AnalyticsConnectorsApi* | [**deleteConnector**](docs/Api/AnalyticsConnectorsApi.md#deleteconnector) | **DELETE** /tenants/{tenantId}/analytics/connectors/{connectorId} | Deletes a connector by Id
*AnalyticsConnectorsApi* | [**getADLSGen2ConnectorById**](docs/Api/AnalyticsConnectorsApi.md#getadlsgen2connectorbyid) | **GET** /tenants/{tenantId}/analytics/connectors/{connectorId} | Retrieves a connector profile by Id
*AnalyticsConnectorsApi* | [**getPaginatedConnectors**](docs/Api/AnalyticsConnectorsApi.md#getpaginatedconnectors) | **GET** /tenants/{tenantId}/analytics/connectors | Retrieves paginated connectors
*AnalyticsConnectorsApi* | [**updateConnector**](docs/Api/AnalyticsConnectorsApi.md#updateconnector) | **PUT** /tenants/{tenantId}/analytics/connectors/{connectorId} | Updates a connector by Id
*AnalyticsDataLakeApi* | [**getPaginatedLakehouseRecords**](docs/Api/AnalyticsDataLakeApi.md#getpaginatedlakehouserecords) | **GET** /tenants/{tenantId}/analytics/datalake/query | Retrieves gold-tier data from the lakehouse
*AnalyticsUserAuthorizationsApi* | [**getPaginatedUserAuthorizations**](docs/Api/AnalyticsUserAuthorizationsApi.md#getpaginateduserauthorizations) | **GET** /tenants/{tenantId}/analytics/userauthorizations | Retrieves paginated user authorizations
*AnalyticsUserAuthorizationsApi* | [**softDeleteUserAuthorization**](docs/Api/AnalyticsUserAuthorizationsApi.md#softdeleteuserauthorization) | **DELETE** /tenants/{tenantId}/analytics/userauthorizations/{userAuthorizationId} | Soft Deletes a user authorization by Id
*ApplicationsApi* | [**getTenantApplicationProfileByIdAsync**](docs/Api/ApplicationsApi.md#gettenantapplicationprofilebyidasync) | **GET** /tenants/{tenantId}/applications/{applicationId} | Retrieves an application
*ApplicationsApi* | [**getTenantApplicationsAsync**](docs/Api/ApplicationsApi.md#gettenantapplicationsasync) | **GET** /tenants/{tenantId}/applications | Retrieves a list of applications associated to this tenant
*ApplicationsSettingsApi* | [**getClientSettingsAsync**](docs/Api/ApplicationsSettingsApi.md#getclientsettingsasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings | Retrieves a list of a Tenant&#39;s ClientSettings.
*ApplicationsSettingsApi* | [**getClientSettingsByCodeAsync**](docs/Api/ApplicationsSettingsApi.md#getclientsettingsbycodeasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings/{code} | Retrieves a Tenant&#39;s ClientSetting by code.
*ApplicationsSettingsApi* | [**getClientSettingsTypesAsync**](docs/Api/ApplicationsSettingsApi.md#getclientsettingstypesasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settingstypes | Retrieves a list of ClientSettingsTypes.
*ApplicationsSettingsApi* | [**setClientSettingsAsync**](docs/Api/ApplicationsSettingsApi.md#setclientsettingsasync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings | Creates/updates a Tenant&#39;s ClientSettings.
*ApplicationsSettingsApi* | [**setClientSettingsByCodeAsync**](docs/Api/ApplicationsSettingsApi.md#setclientsettingsbycodeasync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings/{code} | Creates/updates a Tenant&#39;s ClientSetting by code.
*ApplicationsTilesApi* | [**getTenantApplicationTilesAsync**](docs/Api/ApplicationsTilesApi.md#gettenantapplicationtilesasync) | **GET** /tenants/{tenantId}/applicationtiles | Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant
*CacheApi* | [**refreshUserProfileCache**](docs/Api/CacheApi.md#refreshuserprofilecache) | **POST** /me/cache/refresh | Refreshes the user&#39;s profile cache.
*CapacitiesApi* | [**assignMyGroupToCapacity**](docs/Api/CapacitiesApi.md#assignmygrouptocapacity) | **POST** /tenants/{tenantId}/analytics/capacities | Assigns the specified group to the specified capacity.
*CapacitiesApi* | [**getAllAnalyticsPowerBiCapacities**](docs/Api/CapacitiesApi.md#getallanalyticspowerbicapacities) | **GET** /tenants/{tenantId}/analytics/capacities | Retrieves a list of capacities in Power Bi that the user has access to.
*CapacitiesApi* | [**resumeCapacityAsync**](docs/Api/CapacitiesApi.md#resumecapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/resume | Resumes currently suspended capacity
*CapacitiesApi* | [**suspendCapacityAsync**](docs/Api/CapacitiesApi.md#suspendcapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/suspend | Suspends currently active capacity
*CategoriesApi* | [**addCategoryDataSteward**](docs/Api/CategoriesApi.md#addcategorydatasteward) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards | Adds a Data Steward to a Category.
*CategoriesApi* | [**addCategoryDataStewardBulk**](docs/Api/CategoriesApi.md#addcategorydatastewardbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/stewards | Adds a Data Steward to Categories.
*CategoriesApi* | [**certifyCategory**](docs/Api/CategoriesApi.md#certifycategory) | **POST** /tenants/{tenantId}/statereporting/categories/{categoryId}/certify | Certifies a Category.
*CategoriesApi* | [**getDataUsersBulk**](docs/Api/CategoriesApi.md#getdatausersbulk) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/datausers | Get all Data Users
*CategoriesApi* | [**getStateReportingCategories**](docs/Api/CategoriesApi.md#getstatereportingcategories) | **GET** /tenants/{tenantId}/statereporting/categories | Retrieves a list of Categories.
*CategoriesApi* | [**removeCategoryDataOwner**](docs/Api/CategoriesApi.md#removecategorydataowner) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Removes the Data Owner of a Category.
*CategoriesApi* | [**removeCategoryDataSteward**](docs/Api/CategoriesApi.md#removecategorydatasteward) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards/{email} | Removes a Data Steward from a Category.
*CategoriesApi* | [**requestCategoryCertificationReminder**](docs/Api/CategoriesApi.md#requestcategorycertificationreminder) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/certificationreminder | Requests a Certification Reminder to be sent.
*CategoriesApi* | [**setCategoryDataOwner**](docs/Api/CategoriesApi.md#setcategorydataowner) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Sets the Data Owner of a Category.
*CategoriesApi* | [**setCategoryDataOwnerBulk**](docs/Api/CategoriesApi.md#setcategorydataownerbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/owner | Sets the Data Owner of Categories.
*CategoriesApi* | [**uploadStateReportingCategory**](docs/Api/CategoriesApi.md#uploadstatereportingcategory) | **POST** /tenants/{tenantId}/statereporting/categories/upload | Upload a Category via a JSON file.
*CategoriesApi* | [**uploadStateReportingPeriodsFromCategoryJson**](docs/Api/CategoriesApi.md#uploadstatereportingperiodsfromcategoryjson) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/upload | Upload a Category via a JSON file.
*ChangeLogsApi* | [**getAllChangesAsync**](docs/Api/ChangeLogsApi.md#getallchangesasync) | **GET** /tenants/{tenantId}/changes | 
*ClientsSecretsApi* | [**addClientSecret**](docs/Api/ClientsSecretsApi.md#addclientsecret) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/secrets | Creates a new secret for an OpenId client
*ClientsSecretsApi* | [**regenerateOneRosterApiClientSecretAsync**](docs/Api/ClientsSecretsApi.md#regenerateonerosterapiclientsecretasync) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/regeneratesecret | Regenerate Client Secret
*CollectionsApi* | [**createCollection**](docs/Api/CollectionsApi.md#createcollection) | **POST** /tenants/{tenantId}/validations/collections | Creates a Collection.
*CollectionsApi* | [**createContainer**](docs/Api/CollectionsApi.md#createcontainer) | **POST** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Creates a Container.
*CollectionsApi* | [**deleteCollection**](docs/Api/CollectionsApi.md#deletecollection) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId} | Deletes a Collection.
*CollectionsApi* | [**deleteContainer**](docs/Api/CollectionsApi.md#deletecontainer) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Deletes a Container.
*CollectionsApi* | [**getCollectionById**](docs/Api/CollectionsApi.md#getcollectionbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId} | Retrieves a Collection by ID.
*CollectionsApi* | [**getCollectionJson**](docs/Api/CollectionsApi.md#getcollectionjson) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/export | Retrieves the JSON representation of a Collection. Useful for exporting into other systems.
*CollectionsApi* | [**getCollections**](docs/Api/CollectionsApi.md#getcollections) | **GET** /tenants/{tenantId}/validations/collections | Retrieves a list of Collections.
*CollectionsApi* | [**getCollectionsTree**](docs/Api/CollectionsApi.md#getcollectionstree) | **GET** /tenants/{tenantId}/validations/categories/tree | Retrieves a list of Collections.
*CollectionsApi* | [**getContainerById**](docs/Api/CollectionsApi.md#getcontainerbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Retrieves a Container by ID.
*CollectionsApi* | [**getContainers**](docs/Api/CollectionsApi.md#getcontainers) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Retrieves a list of Containers.
*CollectionsApi* | [**updateCollection**](docs/Api/CollectionsApi.md#updatecollection) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId} | Updates a Collection.
*CollectionsApi* | [**updateContainer**](docs/Api/CollectionsApi.md#updatecontainer) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Updates a Container.
*CollectionsApi* | [**uploadCollectionJson**](docs/Api/CollectionsApi.md#uploadcollectionjson) | **POST** /tenants/{tenantId}/validations/collections/import | Uploads a Collection JSON. Useful for importing from another system.
*ConfigurationsApi* | [**createAnalyticsConfigurationAsync**](docs/Api/ConfigurationsApi.md#createanalyticsconfigurationasync) | **POST** /tenants/{tenantId}/analytics/configurations | Creates a new configuration.
*ConfigurationsApi* | [**deleteAnalyticsConfigurationAsync**](docs/Api/ConfigurationsApi.md#deleteanalyticsconfigurationasync) | **DELETE** /tenants/{tenantId}/analytics/configurations/{configurationId} | Deletes a configuration.
*ConfigurationsApi* | [**getAllAnalyticsConfigurationsAsync**](docs/Api/ConfigurationsApi.md#getallanalyticsconfigurationsasync) | **GET** /tenants/{tenantId}/analytics/configurations | Retrieves all configurations.
*ConfigurationsApi* | [**getAnalyticsConfigurationByIdAsync**](docs/Api/ConfigurationsApi.md#getanalyticsconfigurationbyidasync) | **GET** /tenants/{tenantId}/analytics/configurations/{configurationId} | Retrieves a configuration by ID.
*ConfigurationsApi* | [**getAnalyticsConfigurationByTenantIdAsync**](docs/Api/ConfigurationsApi.md#getanalyticsconfigurationbytenantidasync) | **GET** /tenants/{tenantId}/analytics/configurations/default | Retrieves current default configuration.
*ConfigurationsApi* | [**hasValidAnalyticsConfigurationAsync**](docs/Api/ConfigurationsApi.md#hasvalidanalyticsconfigurationasync) | **GET** /tenants/{tenantId}/analytics/configurations/default/valid | Verifies if current default configuration has required values for correct functionality.
*ConfigurationsApi* | [**updateAnalyticsConfigurationAsync**](docs/Api/ConfigurationsApi.md#updateanalyticsconfigurationasync) | **PUT** /tenants/{tenantId}/analytics/configurations/{configurationId} | Updates a configuration.
*ConfigurationsApi* | [**validateAADTokenAsync**](docs/Api/ConfigurationsApi.md#validateaadtokenasync) | **POST** /tenants/{tenantId}/analytics/configurations/azure/testconnection | Verifies if AAD token generation is possible with user provided values.
*ConnectionsApi* | [**connectionTestedResponse**](docs/Api/ConnectionsApi.md#connectiontestedresponse) | **POST** /tenants/{tenantId}/datasync/connections/testconnection | Tests availability of provided connection metadata.
*ConnectionsApi* | [**createEdFiConnection**](docs/Api/ConnectionsApi.md#createedficonnection) | **POST** /tenants/{tenantId}/edfiadmin/connections | Creates a new Ed-Fi Connection.
*ConnectionsApi* | [**createTenantDataSyncConnection**](docs/Api/ConnectionsApi.md#createtenantdatasyncconnection) | **POST** /tenants/{tenantId}/datasync/connections | Creates a new DataSync connection
*ConnectionsApi* | [**deleteEdFiConnection**](docs/Api/ConnectionsApi.md#deleteedficonnection) | **DELETE** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Deletes an Ed-Fi Connection.
*ConnectionsApi* | [**deleteTenantDataSyncConnection**](docs/Api/ConnectionsApi.md#deletetenantdatasyncconnection) | **DELETE** /tenants/{tenantId}/datasync/connections/{connectionId} | Delete a DataSync connection matching the primary key
*ConnectionsApi* | [**getAllTenantDataSyncConnections**](docs/Api/ConnectionsApi.md#getalltenantdatasyncconnections) | **GET** /tenants/{tenantId}/datasync/connections | Retrieves a list of DataSync Connections
*ConnectionsApi* | [**getConnectionById**](docs/Api/ConnectionsApi.md#getconnectionbyid) | **GET** /tenants/{tenantId}/oneroster/connections/{connectionId} | Retrieves the profile of a Connection.
*ConnectionsApi* | [**getEdFiConnectionById**](docs/Api/ConnectionsApi.md#getedficonnectionbyid) | **GET** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Retrieves an Ed-Fi Connection by ID.
*ConnectionsApi* | [**getEdFiConnectionsAsync**](docs/Api/ConnectionsApi.md#getedficonnectionsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections | Retrieves a list of Ed-Fi Connections.
*ConnectionsApi* | [**getEdFiOdsBackupCodesDescriptorsAsync**](docs/Api/ConnectionsApi.md#getedfiodsbackupcodesdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections/odsbackupcodes | Retrieves a list of Ed-Fi ODS backup codes.
*ConnectionsApi* | [**getPagedConnections**](docs/Api/ConnectionsApi.md#getpagedconnections) | **GET** /tenants/{tenantId}/oneroster/connections | Retrieves a list of Connections.
*ConnectionsApi* | [**getTenantDataSyncConnectionProfileById**](docs/Api/ConnectionsApi.md#gettenantdatasyncconnectionprofilebyid) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId} | Retrieves a specific DataSync connection using its primary key
*ConnectionsApi* | [**testConnectionDetailsAsync**](docs/Api/ConnectionsApi.md#testconnectiondetailsasync) | **POST** /tenants/{tenantId}/oneroster/connections/test | Tests the connection by sending the connection details in the request payload
*ConnectionsApi* | [**testConnectionDetailsByIdAsync**](docs/Api/ConnectionsApi.md#testconnectiondetailsbyidasync) | **POST** /tenants/{tenantId}/oneroster/connections/{connectionId}/test | Tests the connection by obtaining the details by ID
*ConnectionsApi* | [**updateEdFiConnection**](docs/Api/ConnectionsApi.md#updateedficonnection) | **PUT** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Updates an Ed-Fi Connection.
*ConnectionsApi* | [**updateTenantDataSyncConnection**](docs/Api/ConnectionsApi.md#updatetenantdatasyncconnection) | **PUT** /tenants/{tenantId}/datasync/connections/{connectionId} | Updates a DataSync connection matching the primary key
*ConnectionsByTypeDEPRECATEDApi* | [**createOrUpdateStateReportingConnectionByTypeV1**](docs/Api/ConnectionsByTypeDEPRECATEDApi.md#createorupdatestatereportingconnectionbytypev1) | **PUT** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType.
*ConnectionsByTypeDEPRECATEDApi* | [**deleteStateReportingByTypeConnectionV1**](docs/Api/ConnectionsByTypeDEPRECATEDApi.md#deletestatereportingbytypeconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Deletes a Connection by Type
*ConnectionsByTypeDEPRECATEDApi* | [**getStateReportingConnectionByTypeV1**](docs/Api/ConnectionsByTypeDEPRECATEDApi.md#getstatereportingconnectionbytypev1) | **GET** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Retrieves a Connection by Type.
*ConnectionsDEPRECATEDApi* | [**createStateReportingConnectionV1**](docs/Api/ConnectionsDEPRECATEDApi.md#createstatereportingconnectionv1) | **POST** /tenants/{tenantId}/statereporting/connections | Creates a new Connection.
*ConnectionsDEPRECATEDApi* | [**deleteStateReportingConnectionV1**](docs/Api/ConnectionsDEPRECATEDApi.md#deletestatereportingconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connections/{connectionId} | Deletes a Connection.
*ConnectionsDEPRECATEDApi* | [**findStateReportingConnectionsV1**](docs/Api/ConnectionsDEPRECATEDApi.md#findstatereportingconnectionsv1) | **GET** /tenants/{tenantId}/statereporting/connections | Retrieves a list of Connections.
*ConnectionsDEPRECATEDApi* | [**getStateReportingConnectionV1**](docs/Api/ConnectionsDEPRECATEDApi.md#getstatereportingconnectionv1) | **GET** /tenants/{tenantId}/statereporting/connections/{connectionId} | Retrieves a Connection by ID.
*ConnectionsDEPRECATEDApi* | [**testStateReportingConnectionByIdV1**](docs/Api/ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbyidv1) | **POST** /tenants/{tenantId}/statereporting/connections/{connectionId}/testconnection | Tests a Connection by ID.
*ConnectionsDEPRECATEDApi* | [**testStateReportingConnectionByTypeV1**](docs/Api/ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbytypev1) | **POST** /tenants/{tenantId}/statereporting/connections/testconnection | Tests a Connection by Type.
*ConnectionsDEPRECATEDApi* | [**updateStateReportingConnectionV1**](docs/Api/ConnectionsDEPRECATEDApi.md#updatestatereportingconnectionv1) | **PUT** /tenants/{tenantId}/statereporting/connections/{connectionId} | Updates a Connection.
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiDistricts**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfidistricts) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/districts | Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfieducationorganizationiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/educationorganizationidentificationsystemdescriptors | Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiSchoolYears**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfischoolyears) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/schoolyears | Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiStaffIdDescriptors**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistaffiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/staffidentificationsystemdescriptors | Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiStudentIdDescriptors**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistudentiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/studentidentificationsystemdescriptors | Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiTermDescriptors**](docs/Api/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfitermdescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/termdescriptors | Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata
*DomainsApi* | [**createTenantDomainAsync**](docs/Api/DomainsApi.md#createtenantdomainasync) | **POST** /tenants/{tenantId}/domains | Creates a new domain
*DomainsApi* | [**deleteTenantDomainAsync**](docs/Api/DomainsApi.md#deletetenantdomainasync) | **DELETE** /tenants/{tenantId}/domains/{domainName} | Deletes a user
*DomainsApi* | [**getAllTenantDomainsAsync**](docs/Api/DomainsApi.md#getalltenantdomainsasync) | **GET** /tenants/{tenantId}/domains | Retrieves a list of domains associated to this tenant
*DomainsApi* | [**getTenantDomainProfileByNameAsync**](docs/Api/DomainsApi.md#gettenantdomainprofilebynameasync) | **GET** /tenants/{tenantId}/domains/{domainName} | Retrieves a domain
*DomainsApi* | [**updateTenantDomainAsync**](docs/Api/DomainsApi.md#updatetenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName} | Updates a domain
*DomainsApi* | [**verifyTenantDomainAsync**](docs/Api/DomainsApi.md#verifytenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName}/verify | Verify a  tenant&#39;s domain
*EdFiInstancesApi* | [**getAllEdFiAdminConnectionsFromAnalyticsAsync**](docs/Api/EdFiInstancesApi.md#getalledfiadminconnectionsfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/connections | Retrieves a list of EdFi Admin connections
*EdFiInstancesApi* | [**getAllEdFiAdminInstancesFromAnalyticsAsync**](docs/Api/EdFiInstancesApi.md#getalledfiadmininstancesfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances | Retrieves a list of EdFi Admin instances
*EdFiInstancesApi* | [**getEdFiAdminInstanceByIdFromAnalyticsAsync**](docs/Api/EdFiInstancesApi.md#getedfiadmininstancebyidfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances/{instanceId} | Retrieves an Ed-Fi Admin instance by ID.
*EdFiSyncApi* | [**createEdFiSync**](docs/Api/EdFiSyncApi.md#createedfisync) | **POST** /tenants/{tenantId}/jobs/edfisync | Creates an Ed-Fi Sync Job for a given tenant
*EdFiSyncApi* | [**executeEdFiSyncJob**](docs/Api/EdFiSyncApi.md#executeedfisyncjob) | **PUT** /tenants/{tenantId}/jobs/edfisync/execute | Executes an Ed-Fi Sync Job
*EdFiSyncApi* | [**getEdFiSyncData**](docs/Api/EdFiSyncApi.md#getedfisyncdata) | **GET** /tenants/{tenantId}/jobs/edfisync | Retrieves Ed-Fi Sync Connection Data for a given tenant
*EdFiSyncApi* | [**updateEdFiSync**](docs/Api/EdFiSyncApi.md#updateedfisync) | **PUT** /tenants/{tenantId}/jobs/edfisync | Updates an Ed-Fi Sync for a given tenant
*EnvironmentsApi* | [**createEnvironment**](docs/Api/EnvironmentsApi.md#createenvironment) | **POST** /tenants/{tenantId}/validations/environments | Creates an Environment.
*EnvironmentsApi* | [**createStateReportingEnvironment**](docs/Api/EnvironmentsApi.md#createstatereportingenvironment) | **POST** /tenants/{tenantId}/statereporting/environments | Creates a new Environment.
*EnvironmentsApi* | [**deleteEnvironment**](docs/Api/EnvironmentsApi.md#deleteenvironment) | **DELETE** /tenants/{tenantId}/validations/environments/{environmentId} | Deletes an Environment.
*EnvironmentsApi* | [**deleteStateReportingEnvironment**](docs/Api/EnvironmentsApi.md#deletestatereportingenvironment) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId} | Deletes an Environment.
*EnvironmentsApi* | [**getEnvironmentById**](docs/Api/EnvironmentsApi.md#getenvironmentbyid) | **GET** /tenants/{tenantId}/validations/environments/{environmentId} | Retrieves an Environment by ID.
*EnvironmentsApi* | [**getEnvironments**](docs/Api/EnvironmentsApi.md#getenvironments) | **GET** /tenants/{tenantId}/validations/environments | Retrieves a list of Environments.
*EnvironmentsApi* | [**getStateReportingEnvironment**](docs/Api/EnvironmentsApi.md#getstatereportingenvironment) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId} | Retrieves an Environment by ID.
*EnvironmentsApi* | [**searchStateReportingEnvironments**](docs/Api/EnvironmentsApi.md#searchstatereportingenvironments) | **GET** /tenants/{tenantId}/statereporting/environments | Retrieves a list of Environments.
*EnvironmentsApi* | [**testEnvironmentConnection**](docs/Api/EnvironmentsApi.md#testenvironmentconnection) | **POST** /tenants/{tenantId}/validations/environments/testconnection | Tests if the provided connection string can establish a valid connection.
*EnvironmentsApi* | [**updateEnvironment**](docs/Api/EnvironmentsApi.md#updateenvironment) | **PUT** /tenants/{tenantId}/validations/environments/{environmentId} | Updates an Environment.
*EnvironmentsApi* | [**updateStateReportingEnvironment**](docs/Api/EnvironmentsApi.md#updatestatereportingenvironment) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId} | Updates an Environment.
*EnvironmentsConnectionsApi* | [**createStateReportingConnection**](docs/Api/EnvironmentsConnectionsApi.md#createstatereportingconnection) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Creates a new Connection.
*EnvironmentsConnectionsApi* | [**deleteStateReportingConnection**](docs/Api/EnvironmentsConnectionsApi.md#deletestatereportingconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Deletes a Connection.
*EnvironmentsConnectionsApi* | [**findStateReportingConnections**](docs/Api/EnvironmentsConnectionsApi.md#findstatereportingconnections) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Retrieves a list of Connections.
*EnvironmentsConnectionsApi* | [**getStateReportingConnection**](docs/Api/EnvironmentsConnectionsApi.md#getstatereportingconnection) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Retrieves a Connection by ID.
*EnvironmentsConnectionsApi* | [**testStateReportingConnectionById**](docs/Api/EnvironmentsConnectionsApi.md#teststatereportingconnectionbyid) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId}/testconnection | Tests a Connection by ID.
*EnvironmentsConnectionsApi* | [**testStateReportingConnectionByType**](docs/Api/EnvironmentsConnectionsApi.md#teststatereportingconnectionbytype) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/testconnection | Tests a Connection by Type.
*EnvironmentsConnectionsApi* | [**updateStateReportingConnection**](docs/Api/EnvironmentsConnectionsApi.md#updatestatereportingconnection) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Updates a Connection.
*EnvironmentsConnectionsByTypeApi* | [**createOrUpdateStateReportingConnectionByType**](docs/Api/EnvironmentsConnectionsByTypeApi.md#createorupdatestatereportingconnectionbytype) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType.
*EnvironmentsConnectionsByTypeApi* | [**deleteStateReportingByTypeConnection**](docs/Api/EnvironmentsConnectionsByTypeApi.md#deletestatereportingbytypeconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Deletes a Connection by Type
*EnvironmentsConnectionsByTypeApi* | [**getStateReportingConnectionByType**](docs/Api/EnvironmentsConnectionsByTypeApi.md#getstatereportingconnectionbytype) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Retrieves a Connection by Type.
*EnvironmentsReportingPeriodsApi* | [**cancelStateReportingPeriodRun**](docs/Api/EnvironmentsReportingPeriodsApi.md#cancelstatereportingperiodrun) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Cancel the Validation Run of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**closeStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#closestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/close | Closes a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**createStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#createstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Creates a new Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**deleteStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#deletestatereportingperiod) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Deletes a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#getstatereportingperiod) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Retrieves a Reporting Period by ID.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodCertificationStatus**](docs/Api/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodValidationSummary**](docs/Api/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodValidationSummaryByCategory**](docs/Api/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummarybycategory) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of Reporting Period by Category.
*EnvironmentsReportingPeriodsApi* | [**postStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#poststatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/post | Posts a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**runStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#runstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Run a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**searchStateReportingPeriods**](docs/Api/EnvironmentsReportingPeriodsApi.md#searchstatereportingperiods) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Retrieves a list of Reporting Periods.
*EnvironmentsReportingPeriodsApi* | [**setStateReportingPeriodCurrentStep**](docs/Api/EnvironmentsReportingPeriodsApi.md#setstatereportingperiodcurrentstep) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/current | Sets the current step of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**setStateReportingPeriodStepStatus**](docs/Api/EnvironmentsReportingPeriodsApi.md#setstatereportingperiodstepstatus) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/{stepNumber} | Sets the status of a Reporting Period step.
*EnvironmentsReportingPeriodsApi* | [**toggleStateReportingPeriodSelected**](docs/Api/EnvironmentsReportingPeriodsApi.md#togglestatereportingperiodselected) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**updateStateReportingPeriod**](docs/Api/EnvironmentsReportingPeriodsApi.md#updatestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Updates a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**updateStateReportingPeriodBulk**](docs/Api/EnvironmentsReportingPeriodsApi.md#updatestatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Updates Reporting Periods in bulk.
*EnvironmentsReportingPeriodsCategoriesApi* | [**searchStateReportingPeriodCategories**](docs/Api/EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories | Retrieves the Categories of a Reporting Period.
*EnvironmentsReportingPeriodsCategoriesApi* | [**searchStateReportingPeriodSubCategories**](docs/Api/EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodsubcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories/{categoryId}/subcategories | Retrieves the Sub-Categories of a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**deleteStateReportingPeriodRules**](docs/Api/EnvironmentsReportingPeriodsRulesRecordsApi.md#deletestatereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules | Deletes the Rules of a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**searchStateReportingPeriodRecords**](docs/Api/EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**searchStateReportingPeriodRuleRecords**](docs/Api/EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**setStateReportingPeriodRuleRecordPostFlag**](docs/Api/EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflag) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/{recordId}/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Record.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**setStateReportingPeriodRuleRecordPostFlagBulk**](docs/Api/EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records in bulk.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**addReportingPeriodSubmissionMetricsBulkV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsbulkv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**addReportingPeriodSubmissionMetricsV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**cancelReportingPeriodSubmissionV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#cancelreportingperiodsubmissionv2) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionLatestV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlatestv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionLogsV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlogsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionMetricsV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionmetricsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getStateReportingPeriodSubmissionsV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#getstatereportingperiodsubmissionsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**setReportingPeriodSubmissionStatusV2**](docs/Api/EnvironmentsReportingPeriodsSubmissionsApi.md#setreportingperiodsubmissionstatusv2) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission.
*EvaluationSettingsApi* | [**getEvaluationSetting**](docs/Api/EvaluationSettingsApi.md#getevaluationsetting) | **GET** /tenants/{tenantId}/evaluations/configuration | Gets the Evaluation Settings for a given tenant
*EvaluationSettingsApi* | [**setEvaluationSettingApplicationSetting**](docs/Api/EvaluationSettingsApi.md#setevaluationsettingapplicationsetting) | **POST** /tenants/{tenantId}/evaluations/configuration/application | Sets the Application Settings of an Evaluation for a given Tenant
*EvaluationSettingsApi* | [**setEvaluationSettingUserSetting**](docs/Api/EvaluationSettingsApi.md#setevaluationsettingusersetting) | **POST** /tenants/{tenantId}/evaluations/configuration/users | Sets the User Settings of an Evaluation for a given Tenant
*EvaluationsApi* | [**createEvaluation**](docs/Api/EvaluationsApi.md#createevaluation) | **POST** /tenants/{tenantId}/evaluations | Creates a new Evaluation for a given tenant
*EvaluationsApi* | [**deleteEvaluation**](docs/Api/EvaluationsApi.md#deleteevaluation) | **DELETE** /tenants/{tenantId}/evaluations/{evaluationId} | Deletes an Evaluation for a given tenant
*EvaluationsApi* | [**getEvaluation**](docs/Api/EvaluationsApi.md#getevaluation) | **GET** /tenants/{tenantId}/evaluations/{evaluationId} | Get an Evaluation for a given tenant
*EvaluationsApi* | [**getEvaluationCount**](docs/Api/EvaluationsApi.md#getevaluationcount) | **GET** /tenants/{tenantId}/evaluations/count | 
*EvaluationsApi* | [**searchEvaluationAppraisers**](docs/Api/EvaluationsApi.md#searchevaluationappraisers) | **GET** /tenants/{tenantId}/evaluations/appraisers | Searches the Appraisers associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationCampuses**](docs/Api/EvaluationsApi.md#searchevaluationcampuses) | **GET** /tenants/{tenantId}/evaluations/campuses | Searches the Campuses associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationForms**](docs/Api/EvaluationsApi.md#searchevaluationforms) | **GET** /tenants/{tenantId}/evaluations/forms | Searches the Forms associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationStaff**](docs/Api/EvaluationsApi.md#searchevaluationstaff) | **GET** /tenants/{tenantId}/evaluations/staff | Searches the Staff associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluations**](docs/Api/EvaluationsApi.md#searchevaluations) | **GET** /tenants/{tenantId}/evaluations | Searches the Evaluations for a given tenant
*EvaluationsApi* | [**updateEvaluation**](docs/Api/EvaluationsApi.md#updateevaluation) | **PUT** /tenants/{tenantId}/evaluations/{evaluationId} | Updates an Evaluation for a given tenant
*FormComponentsApi* | [**getFormComponent**](docs/Api/FormComponentsApi.md#getformcomponent) | **GET** /tenants/{tenantId}/forms/components/{formComponentId} | Get a Form Component.
*FormComponentsApi* | [**searchFormComponents**](docs/Api/FormComponentsApi.md#searchformcomponents) | **GET** /tenants/{tenantId}/forms/components | Search Form Components
*FormsApi* | [**createForm**](docs/Api/FormsApi.md#createform) | **POST** /tenants/{tenantId}/forms | Creates a new Form for a given tenant
*FormsApi* | [**createFullForm**](docs/Api/FormsApi.md#createfullform) | **POST** /tenants/{tenantId}/forms/full | Fully creates a new Form for a given tenant (with Sections and Questions).
*FormsApi* | [**deleteForm**](docs/Api/FormsApi.md#deleteform) | **DELETE** /tenants/{tenantId}/forms/{formId} | Deletes a Form.
*FormsApi* | [**duplicateForm**](docs/Api/FormsApi.md#duplicateform) | **POST** /tenants/{tenantId}/forms/{formId}/duplicate | Duplicates all Form data for a given tenant (with Sections and Questions).
*FormsApi* | [**getForm**](docs/Api/FormsApi.md#getform) | **GET** /tenants/{tenantId}/forms/{formId} | Get Form.
*FormsApi* | [**getFormAccess**](docs/Api/FormsApi.md#getformaccess) | **GET** /tenants/{tenantId}/forms/{formId}/access | Get the Access Type for a Form.
*FormsApi* | [**getFullFormSchema**](docs/Api/FormsApi.md#getfullformschema) | **GET** /tenants/{tenantId}/forms/{formId}/full/schemas | Get a Forms Json and UI React JSON compatible Schema.
*FormsApi* | [**importForm**](docs/Api/FormsApi.md#importform) | **POST** /tenants/{tenantId}/forms/import | Imports all form data for a given tenant.
*FormsApi* | [**searchForms**](docs/Api/FormsApi.md#searchforms) | **GET** /tenants/{tenantId}/forms | Search Forms
*FormsApi* | [**setFormAccess**](docs/Api/FormsApi.md#setformaccess) | **PUT** /tenants/{tenantId}/forms/{formId}/access | Sets the Access Type for a Form.
*FormsApi* | [**updateForm**](docs/Api/FormsApi.md#updateform) | **PUT** /tenants/{tenantId}/forms/{formId} | Updates a Form.
*FormsApi* | [**updateFullForm**](docs/Api/FormsApi.md#updatefullform) | **PUT** /tenants/{tenantId}/forms/{formId}/full | Fully updates a Form for a given tenant (with Sections and Questions).
*GatewaysApi* | [**getAllAnalyticsGatewaysAsync**](docs/Api/GatewaysApi.md#getallanalyticsgatewaysasync) | **GET** /tenants/{tenantId}/analytics/gateways | Retrieves a list of gateways in Power Bi that the user has access to.
*GroupsApi* | [**addUsersToGroupAsync**](docs/Api/GroupsApi.md#adduserstogroupasync) | **POST** /tenants/{tenantId}/analytics/groups/{groupId}/users/bulk | Adds users to group.
*GroupsApi* | [**createAnalyticsPowerBiGroup**](docs/Api/GroupsApi.md#createanalyticspowerbigroup) | **POST** /tenants/{tenantId}/analytics/groups | Creates a group.
*GroupsApi* | [**deleteAnalyticsPowerBiGroup**](docs/Api/GroupsApi.md#deleteanalyticspowerbigroup) | **DELETE** /tenants/{tenantId}/analytics/groups/{groupId} | Deletes a group.
*GroupsApi* | [**getAnalyticsPowerBiGroupUsers**](docs/Api/GroupsApi.md#getanalyticspowerbigroupusers) | **GET** /tenants/{tenantId}/analytics/groups/{groupId}/users | Retrieves all users for a specific group.
*GroupsApi* | [**getGroupsAsync**](docs/Api/GroupsApi.md#getgroupsasync) | **GET** /tenants/{tenantId}/analytics/groups | Retrieves a list of groups.
*InstanceOnboardingStepsApi* | [**createInstanceOnboardingStepAsync**](docs/Api/InstanceOnboardingStepsApi.md#createinstanceonboardingstepasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps | Creates an Onboarding Step.
*InstanceOnboardingStepsApi* | [**updateInstanceOnboardingStepAsync**](docs/Api/InstanceOnboardingStepsApi.md#updateinstanceonboardingstepasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step.
*InstanceResourcesCountApi* | [**getAllInstanceResourcesCountAsync**](docs/Api/InstanceResourcesCountApi.md#getallinstanceresourcescountasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount | Retrieves a paginated list of Instance Resources Count
*InstanceResourcesCountApi* | [**getAllInstanceResourcesCountJson**](docs/Api/InstanceResourcesCountApi.md#getallinstanceresourcescountjson) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount/export | Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.
*InstancesApi* | [**addRelatedInstances**](docs/Api/InstancesApi.md#addrelatedinstances) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/relatedinstances | Add related instances to root instance by Id
*InstancesApi* | [**addSchoolYear**](docs/Api/InstancesApi.md#addschoolyear) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years | Adds an ODS database to an Instance.
*InstancesApi* | [**addSchoolYearRange**](docs/Api/InstancesApi.md#addschoolyearrange) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/bulk | Adds multiple ODS databases to an instance.
*InstancesApi* | [**changeInstanceDatabaseTierAsync**](docs/Api/InstancesApi.md#changeinstancedatabasetierasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/tiers | Changes the selected tier of an ODS database.
*InstancesApi* | [**cloneInstanceAsync**](docs/Api/InstancesApi.md#cloneinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/clone | Clones an instance.
*InstancesApi* | [**createInstance**](docs/Api/InstancesApi.md#createinstance) | **POST** /tenants/{tenantId}/oneroster/instances | Creates a new Instance.
*InstancesApi* | [**createInstanceAsync**](docs/Api/InstancesApi.md#createinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances | Creates a new Instance.
*InstancesApi* | [**deleteInstance**](docs/Api/InstancesApi.md#deleteinstance) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId} | Deletes an Instance.
*InstancesApi* | [**deleteInstanceAsync**](docs/Api/InstancesApi.md#deleteinstanceasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Deletes an Instance.
*InstancesApi* | [**deleteSchoolYearAsync**](docs/Api/InstancesApi.md#deleteschoolyearasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year} | Removes an ODS database from an Instance.
*InstancesApi* | [**getEdFiAdminInstanceEndpoints**](docs/Api/InstancesApi.md#getedfiadmininstanceendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance.
*InstancesApi* | [**getEdFiAdminInstanceYearEndpoints**](docs/Api/InstancesApi.md#getedfiadmininstanceyearendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance.
*InstancesApi* | [**getInstanceById**](docs/Api/InstancesApi.md#getinstancebyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId} | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceByIdAsync**](docs/Api/InstancesApi.md#getinstancebyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceCsvExport**](docs/Api/InstancesApi.md#getinstancecsvexport) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceCsvExportV2**](docs/Api/InstancesApi.md#getinstancecsvexportv2) | **GET** /v2/tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format
*InstancesApi* | [**getInstanceEndpoints**](docs/Api/InstancesApi.md#getinstanceendpoints) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/endpoints | Retrieves the One Roster endpoint URLs of an Instance.
*InstancesApi* | [**getInstancesAsync**](docs/Api/InstancesApi.md#getinstancesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances | Retrieves a list of Instances.
*InstancesApi* | [**getPagedInstances**](docs/Api/InstancesApi.md#getpagedinstances) | **GET** /tenants/{tenantId}/oneroster/instances | Retrieves a list of Instances.
*InstancesApi* | [**getTenantInstancesV2**](docs/Api/InstancesApi.md#gettenantinstancesv2) | **GET** /v2/tenants/{tenantId}/instances | Get list of all instances for a tenant - V2
*InstancesApi* | [**isInstanceCustomIdAvailable**](docs/Api/InstancesApi.md#isinstancecustomidavailable) | **GET** /tenants/{tenantId}/oneroster/instances/isinstancecustomidavailable/{customId} | Validate if instance is available
*InstancesApi* | [**loadApiMetadata**](docs/Api/InstancesApi.md#loadapimetadata) | **POST** /tenants/{tenantId}/edfiadmin/api-metadata | Loads connection metadata.
*InstancesApi* | [**resetInstance**](docs/Api/InstancesApi.md#resetinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/resetinstance | Resets an Instance.
*InstancesApi* | [**resetInstanceAsync**](docs/Api/InstancesApi.md#resetinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/resetinstance | Resets an Instance.
*InstancesApi* | [**resetInstanceCacheAsync**](docs/Api/InstancesApi.md#resetinstancecacheasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetcache | Resets the cache of an Instance and the specified ODS database.
*InstancesApi* | [**resetSchoolYearAsync**](docs/Api/InstancesApi.md#resetschoolyearasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetods | Resets the ODS database with the specified school year.
*InstancesApi* | [**setInstanceIsDefault**](docs/Api/InstancesApi.md#setinstanceisdefault) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/default | Updates the isDefault property for an instance
*InstancesApi* | [**testConnectionDetailsByInstanceIdAsync**](docs/Api/InstancesApi.md#testconnectiondetailsbyinstanceidasync) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/test | Tests the connection by obtaining the details by Instance ID
*InstancesApi* | [**testCredentialsConnection**](docs/Api/InstancesApi.md#testcredentialsconnection) | **POST** /tenants/{tenantId}/edfiadmin/testconnection | Tests availability of provided connection metadata.
*InstancesApi* | [**testInstanceConnection**](docs/Api/InstancesApi.md#testinstanceconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/testconnection | Tests the connection of the Instance.
*InstancesApi* | [**testInstanceYearConnection**](docs/Api/InstancesApi.md#testinstanceyearconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/testconnection | Tests the connection of the Instance.
*InstancesApi* | [**truncateInstance**](docs/Api/InstancesApi.md#truncateinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/truncate | Truncates the Instance&#39;s database
*InstancesApi* | [**updateInstance**](docs/Api/InstancesApi.md#updateinstance) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId} | Updates an Instance.
*InstancesApi* | [**updateInstanceAsync**](docs/Api/InstancesApi.md#updateinstanceasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Updates an Instance.
*InstancesApi* | [**validateCustomIdAvailable**](docs/Api/InstancesApi.md#validatecustomidavailable) | **GET** /tenants/{tenantId}/edfiadmin/instances/validatecustomidavailable/{customId} | Validate if instance is available
*InstancesApplicationsApi* | [**createApplicationAsync**](docs/Api/InstancesApplicationsApi.md#createapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application.
*InstancesApplicationsApi* | [**createApplicationUserAccessAsync**](docs/Api/InstancesApplicationsApi.md#createapplicationuseraccessasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access.
*InstancesApplicationsApi* | [**deleteApplicationAsync**](docs/Api/InstancesApplicationsApi.md#deleteapplicationasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application.
*InstancesApplicationsApi* | [**deleteApplicationUserAccessAsync**](docs/Api/InstancesApplicationsApi.md#deleteapplicationuseraccessasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access.
*InstancesApplicationsApi* | [**getApplicationAccessAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationaccessasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses.
*InstancesApplicationsApi* | [**getApplicationAccessByIdAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationaccessbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID.
*InstancesApplicationsApi* | [**getApplicationApiClientByIdAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationapiclientbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID.
*InstancesApplicationsApi* | [**getApplicationApiClientsAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationapiclientsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application.
*InstancesApplicationsApi* | [**getApplicationByIdAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID.
*InstancesApplicationsApi* | [**getApplicationsAsync**](docs/Api/InstancesApplicationsApi.md#getapplicationsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications.
*InstancesApplicationsApi* | [**regenerateApiClientSecretAsync**](docs/Api/InstancesApplicationsApi.md#regenerateapiclientsecretasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client.
*InstancesApplicationsApi* | [**regenerateApplicationApiClientCredentials**](docs/Api/InstancesApplicationsApi.md#regenerateapplicationapiclientcredentials) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/regenerate | Regenerates an application&#39;s API Client Credentials
*InstancesApplicationsApi* | [**syncApplicationAsync**](docs/Api/InstancesApplicationsApi.md#syncapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s)
*InstancesApplicationsApi* | [**updateApplicationAsync**](docs/Api/InstancesApplicationsApi.md#updateapplicationasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application.
*InstancesApplicationsApi* | [**updateApplicationUserAccessAsync**](docs/Api/InstancesApplicationsApi.md#updateapplicationuseraccessasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access.
*InstancesAuthorizationStrategiesApi* | [**getAuthorizationStrategiesAsync**](docs/Api/InstancesAuthorizationStrategiesApi.md#getauthorizationstrategiesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/authorizationstrategies | Retrieves a list of Authorization Strategies.
*InstancesClaimSetsApi* | [**createClaimSetAsync**](docs/Api/InstancesClaimSetsApi.md#createclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Creates a ClaimSet.
*InstancesClaimSetsApi* | [**deleteClaimSetAsync**](docs/Api/InstancesClaimSetsApi.md#deleteclaimsetasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Deletes a ClaimSet.
*InstancesClaimSetsApi* | [**getClaimSetByIdAsync**](docs/Api/InstancesClaimSetsApi.md#getclaimsetbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Retrieves a ClaimSet by ID.
*InstancesClaimSetsApi* | [**getClaimSetsAsync**](docs/Api/InstancesClaimSetsApi.md#getclaimsetsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Retrieves a list of ClaimSets.
*InstancesClaimSetsApi* | [**getResourceClaimsGridAsync**](docs/Api/InstancesClaimSetsApi.md#getresourceclaimsgridasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/resourceclaims | Retrieves a grid of Resource Claims.
*InstancesClaimSetsApi* | [**syncClaimSetAsync**](docs/Api/InstancesClaimSetsApi.md#syncclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/sync | Copies a Claim Set from one instance to another/other instance(s)
*InstancesClaimSetsApi* | [**updateClaimSetAsync**](docs/Api/InstancesClaimSetsApi.md#updateclaimsetasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Updates a ClaimSet.
*InstancesClientsApi* | [**createClient**](docs/Api/InstancesClientsApi.md#createclient) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Creates a new client
*InstancesClientsApi* | [**deleteClient**](docs/Api/InstancesClientsApi.md#deleteclient) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Deletes a client by Id
*InstancesClientsApi* | [**getClientById**](docs/Api/InstancesClientsApi.md#getclientbyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Retrieves a client by Id
*InstancesClientsApi* | [**getPagedClients**](docs/Api/InstancesClientsApi.md#getpagedclients) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Retrieves a list of clients for a given instance
*InstancesClientsApi* | [**updateClient**](docs/Api/InstancesClientsApi.md#updateclient) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Updates a client by Id
*InstancesDescriptorMappingsApi* | [**createDescriptorMapping**](docs/Api/InstancesDescriptorMappingsApi.md#createdescriptormapping) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Creates a Descriptor Mapping.
*InstancesDescriptorMappingsApi* | [**deleteDescriptorMapping**](docs/Api/InstancesDescriptorMappingsApi.md#deletedescriptormapping) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Deletes a Descriptor Mapping.
*InstancesDescriptorMappingsApi* | [**exportDescriptorMappings**](docs/Api/InstancesDescriptorMappingsApi.md#exportdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/export | Exports all Descriptor Mappings as a JSON file.
*InstancesDescriptorMappingsApi* | [**getDescriptorMappingById**](docs/Api/InstancesDescriptorMappingsApi.md#getdescriptormappingbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Retrieves a Descriptor Mapping by ID.
*InstancesDescriptorMappingsApi* | [**getDescriptorMappings**](docs/Api/InstancesDescriptorMappingsApi.md#getdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Retrieves a list of Descriptors Mappings.
*InstancesDescriptorMappingsApi* | [**importDescriptorMappings**](docs/Api/InstancesDescriptorMappingsApi.md#importdescriptormappings) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/import | Imports Descriptor Mappings from a JSON file.
*InstancesDescriptorMappingsApi* | [**updateDescriptorMapping**](docs/Api/InstancesDescriptorMappingsApi.md#updatedescriptormapping) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Updates a Descriptor Mapping.
*InstancesDescriptorsApi* | [**createDescriptorAsync**](docs/Api/InstancesDescriptorsApi.md#createdescriptorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Creates a Descriptor.
*InstancesDescriptorsApi* | [**deleteDescriptorAsync**](docs/Api/InstancesDescriptorsApi.md#deletedescriptorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Deletes a Descriptor.
*InstancesDescriptorsApi* | [**getDescriptorByIdAsync**](docs/Api/InstancesDescriptorsApi.md#getdescriptorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Retrieves a Descriptor by ID.
*InstancesDescriptorsApi* | [**getDescriptorNamespacesAsync**](docs/Api/InstancesDescriptorsApi.md#getdescriptornamespacesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/namespaces | Retrieves a list of Descriptor Namespaces.
*InstancesDescriptorsApi* | [**getDescriptorsAsync**](docs/Api/InstancesDescriptorsApi.md#getdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Retrieves a list of Descriptors.
*InstancesDescriptorsApi* | [**updateDescriptorAsync**](docs/Api/InstancesDescriptorsApi.md#updatedescriptorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Updates a Descriptor.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**createEducationServiceCenterAsync**](docs/Api/InstancesEducationOrganizationsEducationServiceCentersApi.md#createeducationservicecenterasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters | Creates an EducationServiceCenter.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**deleteEducationServiceCenterAsync**](docs/Api/InstancesEducationOrganizationsEducationServiceCentersApi.md#deleteeducationservicecenterasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Deletes an EducationServiceCenter.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**getEducationServiceCenterByIdAsync**](docs/Api/InstancesEducationOrganizationsEducationServiceCentersApi.md#geteducationservicecenterbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Retrieves an EducationServiceCenter by ID.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**updateEducationServiceCenterAsync**](docs/Api/InstancesEducationOrganizationsEducationServiceCentersApi.md#updateeducationservicecenterasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Updates an EducationServiceCenter.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**createLocalEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#createlocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Creates a LocalEducationAgency.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**deleteLocalEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#deletelocaleducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Deletes a LocalEducationAgency.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**getLocalEducationAgencyByIdAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getlocaleducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Retrieves a LocalEducationAgency by ID.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**getlLocalEducationAgenciesAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getllocaleducationagenciesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Retrieves a list of LocalEducationAgencies.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**syncLocalEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#synclocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId}/sync | Copies a LocalEducationAgency from one instance to another/other instance(s).
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**updateLocalEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#updatelocaleducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Updates a LocalEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**createStateEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsStateEducationAgenciesApi.md#createstateeducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies | Creates a StateEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**deleteStateEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsStateEducationAgenciesApi.md#deletestateeducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Deletes a StateEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**getStateEducationAgencyByIdAsync**](docs/Api/InstancesEducationOrganizationsStateEducationAgenciesApi.md#getstateeducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Retrieves a StateEducationAgency by ID.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**updateStateEducationAgencyAsync**](docs/Api/InstancesEducationOrganizationsStateEducationAgenciesApi.md#updatestateeducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Updates a StateEducationAgency.
*InstancesInstanceApplicationsApi* | [**createInstanceApplication**](docs/Api/InstancesInstanceApplicationsApi.md#createinstanceapplication) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Creates an Instance Application
*InstancesInstanceApplicationsApi* | [**deleteInstanceApplication**](docs/Api/InstancesInstanceApplicationsApi.md#deleteinstanceapplication) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Deletes an Instance Application
*InstancesInstanceApplicationsApi* | [**getInstanceApplicationById**](docs/Api/InstancesInstanceApplicationsApi.md#getinstanceapplicationbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Retrieves an Instance Application by ID.
*InstancesInstanceApplicationsApi* | [**getInstanceApplications**](docs/Api/InstancesInstanceApplicationsApi.md#getinstanceapplications) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Retrieves a paginated list of Instance applications
*InstancesInstanceApplicationsApi* | [**updateInstanceApplication**](docs/Api/InstancesInstanceApplicationsApi.md#updateinstanceapplication) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Updates an Instance Application
*InstancesInstanceApplicationsAPIClientsApi* | [**createInstanceApiClient**](docs/Api/InstancesInstanceApplicationsAPIClientsApi.md#createinstanceapiclient) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Creates an Instance ApiClient
*InstancesInstanceApplicationsAPIClientsApi* | [**deleteInstanceApiClient**](docs/Api/InstancesInstanceApplicationsAPIClientsApi.md#deleteinstanceapiclient) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Deletes an Instance ApiClient
*InstancesInstanceApplicationsAPIClientsApi* | [**getInstanceApiClientById**](docs/Api/InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclientbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Retrieves an Instance ApiClient by ID.
*InstancesInstanceApplicationsAPIClientsApi* | [**getInstanceApiClients**](docs/Api/InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclients) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Retrieves a paginated list of Instance ApiClients
*InstancesInstanceApplicationsAPIClientsApi* | [**updateInstanceApiClient**](docs/Api/InstancesInstanceApplicationsAPIClientsApi.md#updateinstanceapiclient) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Updates an Instance Application ApiClient
*InstancesLogsApi* | [**getInstanceHttpLogs**](docs/Api/InstancesLogsApi.md#getinstancehttplogs) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/logs/http | Retrieves HTTP logs for a given instance
*InstancesReportsApi* | [**generateReportsAsync**](docs/Api/InstancesReportsApi.md#generatereportsasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/generate | Queues a job to generate the report views in the ODS Database.
*InstancesReportsApi* | [**getReportsStatusAsync**](docs/Api/InstancesReportsApi.md#getreportsstatusasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/status | Retrieves the status of the report views in Instance.
*InstancesReportsApi* | [**getSchoolsByTypeReportAsync**](docs/Api/InstancesReportsApi.md#getschoolsbytypereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/schoolsbytype/{localEducationAgencyId} | Retrieves a \&quot;Schools By Type\&quot; report.
*InstancesReportsApi* | [**getStudentEconomicSituationReportAsync**](docs/Api/InstancesReportsApi.md#getstudenteconomicsituationreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentseconomicsituation/{localEducationAgencyId} | Retrieves a \&quot;Students Economic Situation\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByEthnicityReport**](docs/Api/InstancesReportsApi.md#getstudentenrollmentbyethnicityreport) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/ethnicity/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Ethnicity\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByGenderReportAsync**](docs/Api/InstancesReportsApi.md#getstudentenrollmentbygenderreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/gender/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Gender\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByRaceReportAsync**](docs/Api/InstancesReportsApi.md#getstudentenrollmentbyracereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/race/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Race\&quot; report.
*InstancesReportsApi* | [**getStudentsByProgramReportAsync**](docs/Api/InstancesReportsApi.md#getstudentsbyprogramreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentsbyprogram/{localEducationAgencyId} | Retrieves a \&quot;Students By Program\&quot; report.
*InstancesReportsApi* | [**getTotalEnrollmentsReportAsync**](docs/Api/InstancesReportsApi.md#gettotalenrollmentsreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/totalenrollments/{localEducationAgencyId} | Retrieves a \&quot;Total Enrollments\&quot; report.
*InstancesVendorsApi* | [**createVendorAsync**](docs/Api/InstancesVendorsApi.md#createvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Creates a new Vendor.
*InstancesVendorsApi* | [**deleteVendorAsync**](docs/Api/InstancesVendorsApi.md#deletevendorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Deletes a Vendor.
*InstancesVendorsApi* | [**getVendorByIdAsync**](docs/Api/InstancesVendorsApi.md#getvendorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Retrieves a Vendor by ID.
*InstancesVendorsApi* | [**getVendorsAsync**](docs/Api/InstancesVendorsApi.md#getvendorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Retrieves a list of Vendors.
*InstancesVendorsApi* | [**syncVendorAsync**](docs/Api/InstancesVendorsApi.md#syncvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId}/sync | Copies a Vendor from one instance to another/other instance(s).
*InstancesVendorsApi* | [**updateVendorAsync**](docs/Api/InstancesVendorsApi.md#updatevendorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Updates a Vendor.
*IntegrationProductsApi* | [**createIntegrationProduct**](docs/Api/IntegrationProductsApi.md#createintegrationproduct) | **POST** /integrations/products | Creates an Integration Product.
*IntegrationProductsApi* | [**deleteIntegrationProduct**](docs/Api/IntegrationProductsApi.md#deleteintegrationproduct) | **DELETE** /integrations/products/{productId} | Removes an Integration Product.
*IntegrationProductsApi* | [**getIntegrationProduct**](docs/Api/IntegrationProductsApi.md#getintegrationproduct) | **GET** /integrations/products/{productId} | Gets an Integration Product.
*IntegrationProductsApi* | [**searchIntegrationProducts**](docs/Api/IntegrationProductsApi.md#searchintegrationproducts) | **GET** /integrations/products | Search Integration Products.
*IntegrationProductsApi* | [**updateIntegrationProduct**](docs/Api/IntegrationProductsApi.md#updateintegrationproduct) | **PUT** /integrations/products/{productId} | Updates an Integration Product.
*IntegrationTypesApi* | [**createIntegrationType**](docs/Api/IntegrationTypesApi.md#createintegrationtype) | **POST** /integrations/types | Creates an Integration Type.
*IntegrationTypesApi* | [**deleteIntegrationType**](docs/Api/IntegrationTypesApi.md#deleteintegrationtype) | **DELETE** /integrations/types/{typeId} | Removes an Integration Type.
*IntegrationTypesApi* | [**getIntegrationType**](docs/Api/IntegrationTypesApi.md#getintegrationtype) | **GET** /integrations/types/{typeId} | Gets an Integration Type.
*IntegrationTypesApi* | [**searchIntegrationTypes**](docs/Api/IntegrationTypesApi.md#searchintegrationtypes) | **GET** /integrations/types | Search Integration Types.
*IntegrationTypesApi* | [**updateIntegrationType**](docs/Api/IntegrationTypesApi.md#updateintegrationtype) | **PUT** /integrations/types/{typeId} | Updates an Integration Type.
*IntegrationVendorsApi* | [**createIntegrationVendor**](docs/Api/IntegrationVendorsApi.md#createintegrationvendor) | **POST** /integrations/vendors | Creates an Integration Vendor.
*IntegrationVendorsApi* | [**deleteIntegrationVendor**](docs/Api/IntegrationVendorsApi.md#deleteintegrationvendor) | **DELETE** /integrations/vendors/{vendorId} | Removes an Integration Vendor.
*IntegrationVendorsApi* | [**getIntegrationVendor**](docs/Api/IntegrationVendorsApi.md#getintegrationvendor) | **GET** /integrations/vendors/{vendorId} | Gets an Integration Vendor.
*IntegrationVendorsApi* | [**searchIntegrationVendors**](docs/Api/IntegrationVendorsApi.md#searchintegrationvendors) | **GET** /integrations/vendors | Search Integration Vendors.
*IntegrationVendorsApi* | [**updateIntegrationVendor**](docs/Api/IntegrationVendorsApi.md#updateintegrationvendor) | **PUT** /integrations/vendors/{vendorId} | Updates an Integration Vendor.
*InvitationsApi* | [**deleteTenantInvitationAsync**](docs/Api/InvitationsApi.md#deletetenantinvitationasync) | **DELETE** /tenants/{tenantId}/invitations/{invitationId} | Deletes an invitation
*InvitationsApi* | [**getAllTenantInvitationsAsync**](docs/Api/InvitationsApi.md#getalltenantinvitationsasync) | **GET** /tenants/{tenantId}/invitations | Retrieves a list of invitations associated to this tenant
*InvitationsApi* | [**getTenantInvitationByIdAsync**](docs/Api/InvitationsApi.md#gettenantinvitationbyidasync) | **GET** /tenants/{tenantId}/invitations/{invitationId} | Retrieves a specific invitation
*InvitationsApi* | [**sendTenantInvitationAsync**](docs/Api/InvitationsApi.md#sendtenantinvitationasync) | **POST** /tenants/{tenantId}/invitations | Creates and sends an invitation to a user
*JobExecutionLogsApi* | [**getAllTenantDataSyncJobExecutionLogs**](docs/Api/JobExecutionLogsApi.md#getalltenantdatasyncjobexecutionlogs) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions/{jobExecutionId}/logs | Retrieves a list of DataSync Job Execution Logs
*JobExecutionsApi* | [**getAllTenantDataSyncJobExecutions**](docs/Api/JobExecutionsApi.md#getalltenantdatasyncjobexecutions) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions | Retrieves a list of DataSync Job Executions
*JobExecutionsApi* | [**getTenantJobExecutionsByJobId**](docs/Api/JobExecutionsApi.md#gettenantjobexecutionsbyjobid) | **GET** /tenants/{tenantId}/jobs/{jobId}/executions | Gets job executions by a given job Id
*JobTypesApi* | [**getAllTenantDataSyncJobTypes**](docs/Api/JobTypesApi.md#getalltenantdatasyncjobtypes) | **GET** /tenants/{tenantId}/datasync/jobtypes | Retrieves a list of DataSync job types
*JobTypesApi* | [**getTenantDataSyncJobTypeProfileById**](docs/Api/JobTypesApi.md#gettenantdatasyncjobtypeprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobtypes/{jobTypeId} | Retrieves a specific DataSync job type using its primary key
*JobsApi* | [**activateTenantDataSyncJob**](docs/Api/JobsApi.md#activatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/activate | Activate a DataSync job matching the primary key
*JobsApi* | [**cancelJob**](docs/Api/JobsApi.md#canceljob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/cancel | Requests a Job cancellation.
*JobsApi* | [**cancelTenantDataSyncJob**](docs/Api/JobsApi.md#canceltenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/cancel | Cancel a DataSync job matching the primary key
*JobsApi* | [**createJob**](docs/Api/JobsApi.md#createjob) | **POST** /tenants/{tenantId}/validations/jobs | Creates a Job.
*JobsApi* | [**createTenantDataSyncJob**](docs/Api/JobsApi.md#createtenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs | Creates a new DataSync job
*JobsApi* | [**deactivateTenantDataSyncJob**](docs/Api/JobsApi.md#deactivatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/deactivate | Deactivate a DataSync job matching the primary key
*JobsApi* | [**deleteJob**](docs/Api/JobsApi.md#deletejob) | **DELETE** /tenants/{tenantId}/validations/jobs/{jobId} | Deletes a Job.
*JobsApi* | [**deleteTenantDataSyncJob**](docs/Api/JobsApi.md#deletetenantdatasyncjob) | **DELETE** /tenants/{tenantId}/datasync/jobs/{jobId} | Delete a DataSync job matching the primary key
*JobsApi* | [**executeJob**](docs/Api/JobsApi.md#executejob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/execute | Requests a Job execution.
*JobsApi* | [**executeTenantDataSyncJob**](docs/Api/JobsApi.md#executetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/execute | Execute a DataSync job matching the primary key
*JobsApi* | [**getAllTenantDataSyncJobs**](docs/Api/JobsApi.md#getalltenantdatasyncjobs) | **GET** /tenants/{tenantId}/datasync/jobs | Retrieves a list of DataSync Jobs
*JobsApi* | [**getJobById**](docs/Api/JobsApi.md#getjobbyid) | **GET** /tenants/{tenantId}/validations/jobs/{jobId} | Retrieves a Job by ID.
*JobsApi* | [**getJobs**](docs/Api/JobsApi.md#getjobs) | **GET** /tenants/{tenantId}/validations/jobs | Retrieves a list of Jobs.
*JobsApi* | [**getTenantDataSyncJobProfileById**](docs/Api/JobsApi.md#gettenantdatasyncjobprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId} | Retrieves a specific DataSync job using its primary key
*JobsApi* | [**restartJobSchedule**](docs/Api/JobsApi.md#restartjobschedule) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/restart | Requests a Job schedule restart.
*JobsApi* | [**updateJob**](docs/Api/JobsApi.md#updatejob) | **PUT** /tenants/{tenantId}/validations/jobs/{jobId} | Updates a Job.
*JobsApi* | [**updateTenantDataSyncJob**](docs/Api/JobsApi.md#updatetenantdatasyncjob) | **PUT** /tenants/{tenantId}/datasync/jobs/{jobId} | Updates a DataSync job matching the primary key
*LogsApi* | [**getLogs**](docs/Api/LogsApi.md#getlogs) | **GET** /tenants/{tenantId}/validations/logs | Retrieves a list of Logs.
*MyExtensionsApi* | [**removeUserExtension**](docs/Api/MyExtensionsApi.md#removeuserextension) | **DELETE** /me/extensions/{code} | Removes a user&#39;s profile extension.
*MyExtensionsApi* | [**setUserExtension**](docs/Api/MyExtensionsApi.md#setuserextension) | **POST** /me/extensions | Creates or update a user&#39;s profile extension.
*MyPreferencesApi* | [**getUserPreferences**](docs/Api/MyPreferencesApi.md#getuserpreferences) | **GET** /me/preferences | Retrieves the user&#39;s preferences.
*MyPreferencesApi* | [**preference**](docs/Api/MyPreferencesApi.md#preference) | **GET** /me/preferences/{code} | Retrieves a user&#39;s preference by code.
*MyPreferencesApi* | [**updateUserPreferenceAsync**](docs/Api/MyPreferencesApi.md#updateuserpreferenceasync) | **POST** /me/preferences | Creates or update a user&#39;s preference.
*MyProfileApi* | [**getMyProfile**](docs/Api/MyProfileApi.md#getmyprofile) | **GET** /v2/me | Get the profile of the user that is currently logged in.
*MyProfileApi* | [**getMyTenant**](docs/Api/MyProfileApi.md#getmytenant) | **GET** /v2/me/tenants/{tenantId} | Get the tenant associated to the user.
*MyProfileApi* | [**getUserCacheAsync**](docs/Api/MyProfileApi.md#getusercacheasync) | **GET** /me | Retrieves the profile of the user that is currently logged in, including the user&#39;s preferences and its associated tenants
*MyTenantsApi* | [**getUserTenants**](docs/Api/MyTenantsApi.md#getusertenants) | **GET** /me/tenants | Retrieves the Tenants of the User that is currently logged in.
*MyTenantsApi* | [**searchMyLicenses**](docs/Api/MyTenantsApi.md#searchmylicenses) | **GET** /v2/me/tenants/{tenantId}/licenses | Search the user&#39;s licenses.
*MyTenantsApi* | [**searchMyTenants**](docs/Api/MyTenantsApi.md#searchmytenants) | **GET** /v2/me/tenants | Searches tenants associated to the user.
*ObservationSettingsApi* | [**addAvailablePersona**](docs/Api/ObservationSettingsApi.md#addavailablepersona) | **POST** /tenants/{tenantId}/observations/settings/personas | Adds a persona for a given Tenant
*ObservationSettingsApi* | [**getApplicationSettings**](docs/Api/ObservationSettingsApi.md#getapplicationsettings) | **GET** /tenants/{tenantId}/observations/settings/application | Gets the application settings for the tenant
*ObservationSettingsApi* | [**getPaginatedForms**](docs/Api/ObservationSettingsApi.md#getpaginatedforms) | **GET** /tenants/{tenantId}/observations/forms | Get Paginated Forms
*ObservationSettingsApi* | [**getPaginatedPersonas**](docs/Api/ObservationSettingsApi.md#getpaginatedpersonas) | **GET** /tenants/{tenantId}/observations/settings/personas | Gets available personas
*ObservationSettingsApi* | [**getPaginatedStaffClassifications**](docs/Api/ObservationSettingsApi.md#getpaginatedstaffclassifications) | **GET** /tenants/{tenantId}/observations/settings/available-staffclassifications | Get Paginated Available StaffClassifications
*ObservationSettingsApi* | [**getStaffClassificationsSettings**](docs/Api/ObservationSettingsApi.md#getstaffclassificationssettings) | **GET** /tenants/{tenantId}/observations/settings/staffclassifications | Gets the staffClassification settings for the tenant
*ObservationSettingsApi* | [**getTEATenantOrganizations**](docs/Api/ObservationSettingsApi.md#getteatenantorganizations) | **GET** /tenants/{tenantId}/observations/tenantorganizations | Get TEA tenant organizations
*ObservationSettingsApi* | [**setApplicationSettings**](docs/Api/ObservationSettingsApi.md#setapplicationsettings) | **POST** /tenants/{tenantId}/observations/settings/application | Sets the Application Settings of an Observation for a given Tenant
*ObservationSettingsApi* | [**setRolePersonasSettings**](docs/Api/ObservationSettingsApi.md#setrolepersonassettings) | **POST** /tenants/{tenantId}/observations/settings/rolepersonas | Updates personas assigned to a role configuration of the tenants setting
*ObservationSettingsApi* | [**verifySysAdminCredentials**](docs/Api/ObservationSettingsApi.md#verifysysadmincredentials) | **GET** /tenants/{tenantId}/observations/settings/verify-credentials | Gets the staffClassification settings for the tenant
*ObservationsApi* | [**createObservation**](docs/Api/ObservationsApi.md#createobservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant
*ObservationsApi* | [**createObservationSubmission**](docs/Api/ObservationsApi.md#createobservationsubmission) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submit | Creates a submission for an available form referencing an existing observation
*ObservationsApi* | [**deleteObservation**](docs/Api/ObservationsApi.md#deleteobservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant
*ObservationsApi* | [**getDashboard**](docs/Api/ObservationsApi.md#getdashboard) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId} | Get Observation Dashboard
*ObservationsApi* | [**getDashboardPreferences**](docs/Api/ObservationsApi.md#getdashboardpreferences) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard
*ObservationsApi* | [**getEvalueeSections**](docs/Api/ObservationsApi.md#getevalueesections) | **GET** /tenants/{tenantId}/observations/evaluees/{evalueeId}/sections | Gets the Sections of an evaluee.
*ObservationsApi* | [**getFormQuestions**](docs/Api/ObservationsApi.md#getformquestions) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections/{sectionId}/questions | Search Questions
*ObservationsApi* | [**getFormSections**](docs/Api/ObservationsApi.md#getformsections) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections | Search Observation Form Sections
*ObservationsApi* | [**getObservationById**](docs/Api/ObservationsApi.md#getobservationbyid) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant
*ObservationsApi* | [**getObservationDraft**](docs/Api/ObservationsApi.md#getobservationdraft) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Get an observation form&#39;s draft
*ObservationsApi* | [**getObservationSubmission**](docs/Api/ObservationsApi.md#getobservationsubmission) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submission | Gets a submission for a specific observation
*ObservationsApi* | [**getPaginatedAvailableCampuses**](docs/Api/ObservationsApi.md#getpaginatedavailablecampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses
*ObservationsApi* | [**getPaginatedAvailableForms**](docs/Api/ObservationsApi.md#getpaginatedavailableforms) | **GET** /tenants/{tenantId}/observations/available-forms | Get Paginated Available Forms
*ObservationsApi* | [**getPaginatedCampusSections**](docs/Api/ObservationsApi.md#getpaginatedcampussections) | **GET** /tenants/{tenantId}/observations/campuses/{campusId}/sections | Retrieves a list of Sections for a given available campus.
*ObservationsApi* | [**getPaginatedEvaluees**](docs/Api/ObservationsApi.md#getpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees
*ObservationsApi* | [**getPaginatedObservations**](docs/Api/ObservationsApi.md#getpaginatedobservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant
*ObservationsApi* | [**getSubmittedObservationsCount**](docs/Api/ObservationsApi.md#getsubmittedobservationscount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count
*ObservationsApi* | [**saveDashboardPreferences**](docs/Api/ObservationsApi.md#savedashboardpreferences) | **POST** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard
*ObservationsApi* | [**searchPaginatedEvaluees**](docs/Api/ObservationsApi.md#searchpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/search/evaluees | Search paginated evaluees
*ObservationsApi* | [**updateObservation**](docs/Api/ObservationsApi.md#updateobservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Update an Observation for a given tenant
*ObservationsApi* | [**upsertObservationDraft**](docs/Api/ObservationsApi.md#upsertobservationdraft) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Creates a draft for an observation forms
*ObservationsApi* | [**verifyDashboardAccess**](docs/Api/ObservationsApi.md#verifydashboardaccess) | **POST** /tenants/{tenantId}/observations/dashboards/access | Verify user access to dashboards
*OnboardingStepsApi* | [**createOnboardingStep**](docs/Api/OnboardingStepsApi.md#createonboardingstep) | **POST** /tenants/{tenantId}/onboardingsteps | Creates an Onboarding Step.
*OnboardingStepsApi* | [**getOnboardingSteps**](docs/Api/OnboardingStepsApi.md#getonboardingsteps) | **GET** /tenants/{tenantId}/onboardingsteps | Gets a list of Onboarding Steps.
*OnboardingStepsApi* | [**updateOnboardingStep**](docs/Api/OnboardingStepsApi.md#updateonboardingstep) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step.
*OnboardingStepsConnectionsApi* | [**createOnboardingStepConnection**](docs/Api/OnboardingStepsConnectionsApi.md#createonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections | Creates an Onboarding Step connection.
*OnboardingStepsConnectionsApi* | [**getOnboardingStepConnectionById**](docs/Api/OnboardingStepsConnectionsApi.md#getonboardingstepconnectionbyid) | **GET** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Get an Onboarding Step connection by Id
*OnboardingStepsConnectionsApi* | [**updateOnboardingStepConnection**](docs/Api/OnboardingStepsConnectionsApi.md#updateonboardingstepconnection) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Update an Onboarding Step connection by Id
*OrganizationsApi* | [**createOrganizationAsync**](docs/Api/OrganizationsApi.md#createorganizationasync) | **POST** /tenants/{tenantId}/organizations | Creates an Organization.
*OrganizationsApi* | [**deleteOrganizationAsync**](docs/Api/OrganizationsApi.md#deleteorganizationasync) | **DELETE** /tenants/{tenantId}/organizations/{organizationIdentifier} | Deletes an Organization.
*OrganizationsApi* | [**getOrganizationByIdAsync**](docs/Api/OrganizationsApi.md#getorganizationbyidasync) | **GET** /tenants/{tenantId}/organizations/{organizationIdentifier} | Retrieves an Organization by ID.
*OrganizationsApi* | [**getOrganizationsAsync**](docs/Api/OrganizationsApi.md#getorganizationsasync) | **GET** /tenants/{tenantId}/organizations | Retrieves a list of Organizations.
*OrganizationsApi* | [**updateOrganizationAsync**](docs/Api/OrganizationsApi.md#updateorganizationasync) | **PUT** /tenants/{tenantId}/organizations/{organizationIdentifier} | Updates an Organization.
*PartnershipsApi* | [**getAllPartnerships**](docs/Api/PartnershipsApi.md#getallpartnerships) | **GET** /tenants/{tenantId}/partnerships | Retrieves a list of Partnerships.
*PartnershipsApi* | [**getPartnershipById**](docs/Api/PartnershipsApi.md#getpartnershipbyid) | **GET** /tenants/{tenantId}/partnerships/{partnershipId} | Retrieves a Partnership by ID.
*ProvidersApi* | [**getAllTenantDataSyncProviders**](docs/Api/ProvidersApi.md#getalltenantdatasyncproviders) | **GET** /tenants/{tenantId}/datasync/providers | Retrieves a list of DataSync providers
*ProvidersApi* | [**getTenantDataSyncProviderProfileById**](docs/Api/ProvidersApi.md#gettenantdatasyncproviderprofilebyid) | **GET** /tenants/{tenantId}/datasync/providers/{providerId} | Retrieves a specific DataSync provider using its primary key
*QuestionsApi* | [**createQuestion**](docs/Api/QuestionsApi.md#createquestion) | **POST** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Creates a new Question for a given section
*QuestionsApi* | [**deleteQuestion**](docs/Api/QuestionsApi.md#deletequestion) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Deletes a Question.
*QuestionsApi* | [**getQuestion**](docs/Api/QuestionsApi.md#getquestion) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Get Question.
*QuestionsApi* | [**searchQuestions**](docs/Api/QuestionsApi.md#searchquestions) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Search Questions
*QuestionsApi* | [**updateQuestion**](docs/Api/QuestionsApi.md#updatequestion) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Updates a Question.
*RegistrationsApi* | [**getOnboardingApplicationsAsync**](docs/Api/RegistrationsApi.md#getonboardingapplicationsasync) | **GET** /public/applications | Gets a list of applications available for registration/onboarding
*RegistrationsApi* | [**getRegistrationApprovalStatusAsync**](docs/Api/RegistrationsApi.md#getregistrationapprovalstatusasync) | **GET** /registrations/{registrationId} | Gets the approval status of a registration
*RegistrationsApi* | [**submitTenantRegistrationAsync**](docs/Api/RegistrationsApi.md#submittenantregistrationasync) | **POST** /registrations | Submits a tenant&#39;s registration request
*RegistrationsAzureMarketplaceApi* | [**submitTenantRegistrationAzureMonaAsync**](docs/Api/RegistrationsAzureMarketplaceApi.md#submittenantregistrationazuremonaasync) | **POST** /registrations/azure/mona | Submits a tenant&#39;s registration request received through Azure [M]arketplace [On]boarding [A]ccelerator (MONA)
*ReportingPeriodsApi* | [**addReportingPeriodSubmissionMetrics**](docs/Api/ReportingPeriodsApi.md#addreportingperiodsubmissionmetrics) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission.
*ReportingPeriodsApi* | [**addReportingPeriodSubmissionMetricsBulk**](docs/Api/ReportingPeriodsApi.md#addreportingperiodsubmissionmetricsbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk.
*ReportingPeriodsApi* | [**cancelReportingPeriodSubmission**](docs/Api/ReportingPeriodsApi.md#cancelreportingperiodsubmission) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission.
*ReportingPeriodsApi* | [**closeReportingPeriodAsync**](docs/Api/ReportingPeriodsApi.md#closereportingperiodasync) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/close | Closes the state of a Reporting Period.
*ReportingPeriodsApi* | [**deleteReportingPeriodRules**](docs/Api/ReportingPeriodsApi.md#deletereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules | Delete the Reporting Period and Associated Rules
*ReportingPeriodsApi* | [**getReportingPeriodCertificationStatus**](docs/Api/ReportingPeriodsApi.md#getreportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodRecords**](docs/Api/ReportingPeriodsApi.md#getreportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodRuleRecords**](docs/Api/ReportingPeriodsApi.md#getreportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule.
*ReportingPeriodsApi* | [**getReportingPeriodSubmission**](docs/Api/ReportingPeriodsApi.md#getreportingperiodsubmission) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionLatest**](docs/Api/ReportingPeriodsApi.md#getreportingperiodsubmissionlatest) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionLogs**](docs/Api/ReportingPeriodsApi.md#getreportingperiodsubmissionlogs) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionMetrics**](docs/Api/ReportingPeriodsApi.md#getreportingperiodsubmissionmetrics) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissions**](docs/Api/ReportingPeriodsApi.md#getreportingperiodsubmissions) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodValidationSummary**](docs/Api/ReportingPeriodsApi.md#getreportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodValidationSummaryByCategoryId**](docs/Api/ReportingPeriodsApi.md#getreportingperiodvalidationsummarybycategoryid) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of a Reporting Period for a Category.
*ReportingPeriodsApi* | [**getReportingPeriods**](docs/Api/ReportingPeriodsApi.md#getreportingperiods) | **GET** /tenants/{tenantId}/statereporting/reportingperiods | Retrieves a list of Reporting Periods.
*ReportingPeriodsApi* | [**postReportingPeriod**](docs/Api/ReportingPeriodsApi.md#postreportingperiod) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/post | Post a Reporting Period.
*ReportingPeriodsApi* | [**runReportingPeriodValidations**](docs/Api/ReportingPeriodsApi.md#runreportingperiodvalidations) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/run | Run Reporting Period Validations.
*ReportingPeriodsApi* | [**setReportingPeriodRuleRecordExcludeFromPostFlagBulk**](docs/Api/ReportingPeriodsApi.md#setreportingperiodrulerecordexcludefrompostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records.
*ReportingPeriodsApi* | [**setReportingPeriodSubmissionStatus**](docs/Api/ReportingPeriodsApi.md#setreportingperiodsubmissionstatus) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission.
*ReportingPeriodsApi* | [**toggleReportingPeriodSelection**](docs/Api/ReportingPeriodsApi.md#togglereportingperiodselection) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period.
*ReportingPeriodsApi* | [**updateReportingPeriodBulk**](docs/Api/ReportingPeriodsApi.md#updatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods | Updates Reporting Periods in bulk.
*ReportsApi* | [**createReportAsync**](docs/Api/ReportsApi.md#createreportasync) | **POST** /tenants/{tenantId}/analytics/reports | Creates a new report (Does not upload pbix file).
*ReportsApi* | [**deleteReportAsync**](docs/Api/ReportsApi.md#deletereportasync) | **DELETE** /tenants/{tenantId}/analytics/reports/{reportId} | Removes a report.
*ReportsApi* | [**downloadReportAsync**](docs/Api/ReportsApi.md#downloadreportasync) | **GET** /tenants/{tenantId}/analytics/reports/download/{reportId}/{groupId} | Retrieves the PBIX for any report in the list in order to download
*ReportsApi* | [**getAllTenantAnalyticsWorkspaceReportsAsync**](docs/Api/ReportsApi.md#getalltenantanalyticsworkspacereportsasync) | **GET** /tenants/{tenantId}/analytics/reports | Retrieves all reports.
*ReportsApi* | [**getReportByIdAsync**](docs/Api/ReportsApi.md#getreportbyidasync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId} | Retrieves a Report by ID.
*ReportsApi* | [**syncLatestVersion**](docs/Api/ReportsApi.md#synclatestversion) | **POST** /tenants/{tenantId}/analytics/reports/synclatestversion | Sync latest version
*ReportsApi* | [**syncWorkspacesAsync**](docs/Api/ReportsApi.md#syncworkspacesasync) | **POST** /tenants/{tenantId}/analytics/reports/sync | Triggers workspace, ODS and DW automation.
*ReportsApi* | [**updateReportAsync**](docs/Api/ReportsApi.md#updatereportasync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId} | Updates a report.
*RulesApi* | [**createRule**](docs/Api/RulesApi.md#createrule) | **POST** /tenants/{tenantId}/validations/rules | Creates a Rule.
*RulesApi* | [**deleteRule**](docs/Api/RulesApi.md#deleterule) | **DELETE** /tenants/{tenantId}/validations/rules/{ruleId} | Deletes a Rule.
*RulesApi* | [**getRuleById**](docs/Api/RulesApi.md#getrulebyid) | **GET** /tenants/{tenantId}/validations/rules/{ruleId} | Retrieves a Rule by ID.
*RulesApi* | [**getRules**](docs/Api/RulesApi.md#getrules) | **GET** /tenants/{tenantId}/validations/rules | Retrieves a list of Rules.
*RulesApi* | [**updateRule**](docs/Api/RulesApi.md#updaterule) | **PUT** /tenants/{tenantId}/validations/rules/{ruleId} | Updates a Rule.
*SectionsApi* | [**createSection**](docs/Api/SectionsApi.md#createsection) | **POST** /tenants/{tenantId}/forms/{formId}/sections | Creates a new Section for a given form
*SectionsApi* | [**deleteSection**](docs/Api/SectionsApi.md#deletesection) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Deletes a Section.
*SectionsApi* | [**getSection**](docs/Api/SectionsApi.md#getsection) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Get Section.
*SectionsApi* | [**getSectionAcademicSubjects**](docs/Api/SectionsApi.md#getsectionacademicsubjects) | **GET** /tenants/{tenantId}/sections/academicSubjects | Retrieves a list of Section Academic Subjects.
*SectionsApi* | [**getSectionById**](docs/Api/SectionsApi.md#getsectionbyid) | **GET** /tenants/{tenantId}/sections/{sectionId} | Retrieves a Section by ID.
*SectionsApi* | [**getSectionCourses**](docs/Api/SectionsApi.md#getsectioncourses) | **GET** /tenants/{tenantId}/sections/courses | Retrieves a list of Section Courses.
*SectionsApi* | [**getSectionGradeLevels**](docs/Api/SectionsApi.md#getsectiongradelevels) | **GET** /tenants/{tenantId}/sections/gradeLevels | Retrieves a list of Section Grade Levels.
*SectionsApi* | [**getSectionSchools**](docs/Api/SectionsApi.md#getsectionschools) | **GET** /tenants/{tenantId}/sections/schools | Retrieves a list of Section Schools.
*SectionsApi* | [**getSectionSessions**](docs/Api/SectionsApi.md#getsectionsessions) | **GET** /tenants/{tenantId}/sections/sessions | Retrieves a list of Section Sessions.
*SectionsApi* | [**getSectionTerms**](docs/Api/SectionsApi.md#getsectionterms) | **GET** /tenants/{tenantId}/sections/terms | Retrieves a list of Section Terms.
*SectionsApi* | [**getSections**](docs/Api/SectionsApi.md#getsections) | **GET** /tenants/{tenantId}/sections | Retrieves a list of Sections.
*SectionsApi* | [**searchSections**](docs/Api/SectionsApi.md#searchsections) | **GET** /tenants/{tenantId}/forms/{formId}/sections | Search Sections
*SectionsApi* | [**updateSection**](docs/Api/SectionsApi.md#updatesection) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Updates a Section.
*SettingsApi* | [**getTenantSettingByCode**](docs/Api/SettingsApi.md#gettenantsettingbycode) | **GET** /tenants/{tenantId}/tenantsettings/{code} | Retrieves a Tenant&#39;s settings by code.
*SettingsApi* | [**getTenantSettings**](docs/Api/SettingsApi.md#gettenantsettings) | **GET** /tenants/{tenantId}/settings | Retrieves a list of the Tenant&#39;s settings.
*SettingsApi* | [**getTenantSettingsByCode**](docs/Api/SettingsApi.md#gettenantsettingsbycode) | **GET** /tenants/{tenantId}/settings/{code} | Retrieves a Tenant&#39;s settings by code.
*SettingsApi* | [**setTenantSettings**](docs/Api/SettingsApi.md#settenantsettings) | **POST** /tenants/{tenantId}/settings/{code} | Creates/updates a Tenant&#39;s settings.
*StaffClassificationsApi* | [**createStaffClassification**](docs/Api/StaffClassificationsApi.md#createstaffclassification) | **POST** /tenants/{tenantId}/staffclassifications | Creates a StaffClassification.
*StaffClassificationsApi* | [**deleteStaffClassification**](docs/Api/StaffClassificationsApi.md#deletestaffclassification) | **DELETE** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Deletes a StaffClassification.
*StaffClassificationsApi* | [**getStaffClassificationById**](docs/Api/StaffClassificationsApi.md#getstaffclassificationbyid) | **GET** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Retrieves a StaffClassification by ID.
*StaffClassificationsApi* | [**getStaffClassifications**](docs/Api/StaffClassificationsApi.md#getstaffclassifications) | **GET** /tenants/{tenantId}/staffclassifications | Retrieves a list of StaffClassifications.
*StaffClassificationsApi* | [**getStaffClassificationsNamespaces**](docs/Api/StaffClassificationsApi.md#getstaffclassificationsnamespaces) | **GET** /tenants/{tenantId}/staffclassifications/namespaces | Retrieves a list of unique Staff Classification Namespaces.
*StaffClassificationsApi* | [**updateStaffClassification**](docs/Api/StaffClassificationsApi.md#updatestaffclassification) | **PUT** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Updates a StaffClassification.
*StateReportingStepsApi* | [**getSteps**](docs/Api/StateReportingStepsApi.md#getsteps) | **GET** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Get Steps Status for the tenant.
*StateReportingStepsApi* | [**updateStep**](docs/Api/StateReportingStepsApi.md#updatestep) | **POST** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Update Steps Status for the tenant.
*SubmissionsApi* | [**createSubmission**](docs/Api/SubmissionsApi.md#createsubmission) | **POST** /tenants/{tenantId}/forms/{formId}/submissions | Creates a new Submission for a given question
*SubmissionsApi* | [**deleteSubmission**](docs/Api/SubmissionsApi.md#deletesubmission) | **DELETE** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Deletes a Submission.
*SubmissionsApi* | [**exportSubmissions**](docs/Api/SubmissionsApi.md#exportsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/export | Exports Submission data for a Form for a given tenant. (With JSON and CSV support)
*SubmissionsApi* | [**getSubmission**](docs/Api/SubmissionsApi.md#getsubmission) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Get Submission.
*SubmissionsApi* | [**searchSubmissions**](docs/Api/SubmissionsApi.md#searchsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions | Search Submissions
*SubmissionsApi* | [**updateSubmission**](docs/Api/SubmissionsApi.md#updatesubmission) | **PUT** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Updates a Submission.
*SubscriptionsApi* | [**createTenantSubscriptionAsync**](docs/Api/SubscriptionsApi.md#createtenantsubscriptionasync) | **POST** /tenants/{tenantId}/subscriptions | Creates a new subscription
*SubscriptionsApi* | [**getAllTenantSubscriptionApplications**](docs/Api/SubscriptionsApi.md#getalltenantsubscriptionapplications) | **GET** /tenants/{tenantId}/subscriptions/applications | Retrieves a list of applications available for subscription.
*SubscriptionsApi* | [**getAllTenantSubscriptionsAsync**](docs/Api/SubscriptionsApi.md#getalltenantsubscriptionsasync) | **GET** /tenants/{tenantId}/subscriptions | Retrieves a list of subscriptions associated to this tenant
*SubscriptionsApi* | [**getTenantSubscriptionProfileByIdAsync**](docs/Api/SubscriptionsApi.md#gettenantsubscriptionprofilebyidasync) | **GET** /tenants/{tenantId}/subscriptions/{subscriptionId} | Retrieves a subscription
*SubscriptionsApi* | [**updateTenantSubscriptionAsync**](docs/Api/SubscriptionsApi.md#updatetenantsubscriptionasync) | **PUT** /tenants/{tenantId}/subscriptions/{subscriptionId} | Updates a subscription
*TagsApi* | [**createTag**](docs/Api/TagsApi.md#createtag) | **POST** /tenants/{tenantId}/validations/tags | Creates a Tag.
*TagsApi* | [**deleteTag**](docs/Api/TagsApi.md#deletetag) | **DELETE** /tenants/{tenantId}/validations/tags/{tagId} | Deletes a Tag.
*TagsApi* | [**getTagById**](docs/Api/TagsApi.md#gettagbyid) | **GET** /tenants/{tenantId}/validations/tags/{tagId} | Retrieves a Tag by ID.
*TagsApi* | [**getTags**](docs/Api/TagsApi.md#gettags) | **GET** /tenants/{tenantId}/validations/tags | Retrieves a list of Tags.
*TagsApi* | [**updateTag**](docs/Api/TagsApi.md#updatetag) | **PUT** /tenants/{tenantId}/validations/tags/{tagId} | Updates a Tag.
*TenantBrandingApi* | [**updateTenantBranding**](docs/Api/TenantBrandingApi.md#updatetenantbranding) | **PUT** /tenants/{tenantId}/branding | Updates the branding of tenant
*TenantInstancesApi* | [**loadOnboardingStepEdFiApiMetadata**](docs/Api/TenantInstancesApi.md#loadonboardingstepedfiapimetadata) | **POST** /tenants/{tenantId}/onboardingsteps/edfi-api-metadata | Loads connection metadata.
*TenantInstancesApi* | [**testOnboardingStepConnection**](docs/Api/TenantInstancesApi.md#testonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/testconnection | Tests availability of provided connection metadata.
*TenantIntegrationsApi* | [**addTenantIntegration**](docs/Api/TenantIntegrationsApi.md#addtenantintegration) | **POST** /tenants/{tenantId}/integrations | Creates an Integration for a tenant.
*TenantIntegrationsApi* | [**deleteTenantIntegration**](docs/Api/TenantIntegrationsApi.md#deletetenantintegration) | **DELETE** /tenants/{tenantId}/integrations/{id} | Removes a tenant Integration.
*TenantIntegrationsApi* | [**getTenantIntegration**](docs/Api/TenantIntegrationsApi.md#gettenantintegration) | **GET** /tenants/{tenantId}/integrations/{id} | Gets a tenant Integration.
*TenantIntegrationsApi* | [**searchIntegrations**](docs/Api/TenantIntegrationsApi.md#searchintegrations) | **GET** /tenants/{tenantId}/integrations | Search a Tenant&#39;s Integrations
*TenantIntegrationsApi* | [**updateTenantIntegration**](docs/Api/TenantIntegrationsApi.md#updatetenantintegration) | **PUT** /tenants/{tenantId}/integrations/{id} | Updates a tenant Integration.
*TenantJobsDSLApi* | [**createDslJob**](docs/Api/TenantJobsDSLApi.md#createdsljob) | **POST** /tenants/{tenantId}/jobs/dsl | Creates a DSL Sync Job for a given tenant
*TenantJobsDSLApi* | [**executeDslJob**](docs/Api/TenantJobsDSLApi.md#executedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId}/execute | Executes a DSL Sync Job for a given tenant
*TenantJobsDSLApi* | [**getDslJob**](docs/Api/TenantJobsDSLApi.md#getdsljob) | **GET** /tenants/{tenantId}/jobs/dsl/{jobId} | Retrieves a DSL jobs profile for a given tenant
*TenantJobsDSLApi* | [**updateDslJob**](docs/Api/TenantJobsDSLApi.md#updatedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId} | Updates a DSL Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**createInstructionalInsightsSecuritySyncJob**](docs/Api/TenantJobsInstructionalInsightsApi.md#createinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights | Creates an Instructional Insights Security Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**executeInstructionalInsightsSecuritySyncJob**](docs/Api/TenantJobsInstructionalInsightsApi.md#executeinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights/execute | Executes an Instructional Insights Security Sync Job
*TenantJobsInstructionalInsightsApi* | [**getInstructionalInsightsSecuritySyncJob**](docs/Api/TenantJobsInstructionalInsightsApi.md#getinstructionalinsightssecuritysyncjob) | **GET** /tenants/{tenantId}/jobs/instructionalinsights | Retrieves an Instructional Insights Security Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**searchInstructionalInsightsSecuritySyncJobExecutionLogs**](docs/Api/TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutionlogs) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions/{executionId}/logs | Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution
*TenantJobsInstructionalInsightsApi* | [**searchInstructionalInsightsSecuritySyncJobExecutions**](docs/Api/TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutions) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions | Searches Instructional Insights Security Sync Job Executions for a given tenant
*TenantJobsInstructionalInsightsApi* | [**updateInstructionalInsightsSecuritySyncJob**](docs/Api/TenantJobsInstructionalInsightsApi.md#updateinstructionalinsightssecuritysyncjob) | **PUT** /tenants/{tenantId}/jobs/instructionalinsights | Updates an Instructional Insights Security Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**createSecurityScoreSyncJob**](docs/Api/TenantSecurityScoreSyncApi.md#createsecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore | Creates an Security Score Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**executeSecurityScoreSyncJob**](docs/Api/TenantSecurityScoreSyncApi.md#executesecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore/execute | Executes an Security Score Sync Job
*TenantSecurityScoreSyncApi* | [**getSecurityScoreSyncJob**](docs/Api/TenantSecurityScoreSyncApi.md#getsecurityscoresyncjob) | **GET** /tenants/{tenantId}/jobs/securityscore | Retrieves a Security Score Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**getSecurityScoreSyncJobExecution**](docs/Api/TenantSecurityScoreSyncApi.md#getsecurityscoresyncjobexecution) | **GET** /tenants/{tenantId}/jobs/securityscore/{jobId}/executions/{jobExecutionId} | Retrieves a Security Score Sync Job Execution for a given tenant
*TenantSecurityScoreSyncApi* | [**updateSecurityScoreSyncJob**](docs/Api/TenantSecurityScoreSyncApi.md#updatesecurityscoresyncjob) | **PUT** /tenants/{tenantId}/jobs/securityscore | Updates a Security Score Sync for a given tenant
*TenantSettingTypesApi* | [**getAllSettingTypes**](docs/Api/TenantSettingTypesApi.md#getallsettingtypes) | **GET** /tenants/settings | Retrieves all setting types
*TenantsApi* | [**getTenantByIdAsync**](docs/Api/TenantsApi.md#gettenantbyidasync) | **GET** /tenants/{tenantId} | Retrieves the profile of a specific tenant
*TenantsApi* | [**updateTenantAsync**](docs/Api/TenantsApi.md#updatetenantasync) | **PUT** /tenants/{tenantId} | Updates a tenant&#39;s profile
*UsersApi* | [**activateTenantUserAsync**](docs/Api/UsersApi.md#activatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/activate | Activates a user
*UsersApi* | [**createTenantLocalUserAsync**](docs/Api/UsersApi.md#createtenantlocaluserasync) | **POST** /tenants/{tenantId}/users | Creates a user in the local identity provider
*UsersApi* | [**deactivateTenantUserAsync**](docs/Api/UsersApi.md#deactivatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/deactivate | Deactivates a user
*UsersApi* | [**deleteTenantUserAsync**](docs/Api/UsersApi.md#deletetenantuserasync) | **DELETE** /tenants/{tenantId}/users/{userId} | Deletes a user
*UsersApi* | [**getAllFormUsers**](docs/Api/UsersApi.md#getallformusers) | **GET** /tenants/{tenantId}/forms/users | Get All Users
*UsersApi* | [**getAllTenantUsersAsync**](docs/Api/UsersApi.md#getalltenantusersasync) | **GET** /tenants/{tenantId}/users | Retrieves a list of users associated to this tenant
*UsersApi* | [**getAllUsers**](docs/Api/UsersApi.md#getallusers) | **GET** /tenants/{tenantId}/statereporting/users | Get All Users
*UsersApi* | [**getTenantUser**](docs/Api/UsersApi.md#gettenantuser) | **GET** /v2/tenants/{tenantId}/users/{userId} | Get User
*UsersApi* | [**getTenantUserProfileByIdAsync**](docs/Api/UsersApi.md#gettenantuserprofilebyidasync) | **GET** /tenants/{tenantId}/users/{userId} | Retrieves a user
*UsersApi* | [**getUserTenant**](docs/Api/UsersApi.md#getusertenant) | **GET** /v2/tenants/{tenantId}/users/{userId}/tenant | Get User Tenant
*UsersApi* | [**getUserTenantStatusProfile**](docs/Api/UsersApi.md#getusertenantstatusprofile) | **GET** /tenants/{tenantId}/users/{email}/status | Searches a user by email and retrieves it&#39;s minimal information and status.
*UsersApi* | [**resetMfaStatusAsync**](docs/Api/UsersApi.md#resetmfastatusasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetmfa | Reset the MFA Status for the User
*UsersApi* | [**resetPasswordTenantUserAsync**](docs/Api/UsersApi.md#resetpasswordtenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetpassword | Resets a user&#39;s password
*UsersApi* | [**searchTenantUsers**](docs/Api/UsersApi.md#searchtenantusers) | **GET** /v2/tenants/{tenantId}/users | Search Users
*UsersApi* | [**searchUserLicenses**](docs/Api/UsersApi.md#searchuserlicenses) | **GET** /v2/tenants/{tenantId}/users/{userId}/licenses | Search User Licenses
*UsersApi* | [**searchUserLicensesBulk**](docs/Api/UsersApi.md#searchuserlicensesbulk) | **GET** /v2/tenants/{tenantId}/users/licensesBulk | Search user licenses in bulk.
*UsersApi* | [**updateTenantUserAsync**](docs/Api/UsersApi.md#updatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId} | Creates or updates a user
*UsersEducationOrganizationsApi* | [**addUserEducationOrganization**](docs/Api/UsersEducationOrganizationsApi.md#addusereducationorganization) | **POST** /tenants/{tenantId}/users/{userId}/educationorganizations | Adds an Education Organization to a user.
*UsersEducationOrganizationsApi* | [**getUserEducationOrganizations**](docs/Api/UsersEducationOrganizationsApi.md#getusereducationorganizations) | **GET** /tenants/{tenantId}/users/{userId}/educationorganizations | Gets the Education Organizations of a user.
*UsersEducationOrganizationsApi* | [**removeUserEducationOrganization**](docs/Api/UsersEducationOrganizationsApi.md#removeusereducationorganization) | **DELETE** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Removes an Education Organization from a user.
*UsersEducationOrganizationsApi* | [**updateUserEducationOrganization**](docs/Api/UsersEducationOrganizationsApi.md#updateusereducationorganization) | **PUT** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Updates the Education Organization of a user.
*UsersLicensesApi* | [**assignLicenseTenantUserAsync**](docs/Api/UsersLicensesApi.md#assignlicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assign | Assigns a license to a user in the context of a specific tenant
*UsersLicensesApi* | [**assignLicenseTenantUserBulkAsync**](docs/Api/UsersLicensesApi.md#assignlicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assignbulk | Assigns one or more licenses to a user in the context of a specific tenant
*UsersLicensesApi* | [**getAllTenantUserApplicationLicensesAsync**](docs/Api/UsersLicensesApi.md#getalltenantuserapplicationlicensesasync) | **GET** /tenants/{tenantId}/users/{userId}/licenses | Retrieves a list of user licenses in the context of a specific tenant
*UsersLicensesApi* | [**revokeLicenseTenantUserAsync**](docs/Api/UsersLicensesApi.md#revokelicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revoke | Revokes a license from a user in the context of a specific tenant
*UsersLicensesApi* | [**revokeLicenseTenantUserBulkAsync**](docs/Api/UsersLicensesApi.md#revokelicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revokebulk | Revokes one or more licenses from a user in the context of a specific tenant
*UsersSEOAAsApi* | [**addUserSEOAA**](docs/Api/UsersSEOAAsApi.md#adduserseoaa) | **POST** /v2/tenants/{tenantId}/users/{userId}/seoaas | Add User SEOAAs
*UsersSEOAAsApi* | [**deleteUserSEOAA**](docs/Api/UsersSEOAAsApi.md#deleteuserseoaa) | **DELETE** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Delete User SEOAAs
*UsersSEOAAsApi* | [**searchUserSEOAA**](docs/Api/UsersSEOAAsApi.md#searchuserseoaa) | **GET** /v2/tenants/{tenantId}/users/{userId}/seoaas | Search User SEOAAs
*UsersSEOAAsApi* | [**updateUserSEOAA**](docs/Api/UsersSEOAAsApi.md#updateuserseoaa) | **PUT** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Update User SEOAAs
*UsersSectionsApi* | [**addUserSection**](docs/Api/UsersSectionsApi.md#addusersection) | **POST** /tenants/{tenantId}/users/{userId}/sections | Adds a Section to a user.
*UsersSectionsApi* | [**addUserSectionBulk**](docs/Api/UsersSectionsApi.md#addusersectionbulk) | **POST** /tenants/{tenantId}/users/{userId}/sections/bulk | Adds Sections to a user in bulk.
*UsersSectionsApi* | [**getUserSections**](docs/Api/UsersSectionsApi.md#getusersections) | **GET** /tenants/{tenantId}/users/{userId}/sections | Gets the Sections of a user.
*UsersSectionsApi* | [**removeUserSection**](docs/Api/UsersSectionsApi.md#removeusersection) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Removes a Section from a user.
*UsersSectionsApi* | [**removeUserSectionBulk**](docs/Api/UsersSectionsApi.md#removeusersectionbulk) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/bulk | Removes Sections from a user in bulk.
*UsersSectionsApi* | [**updateUserSection**](docs/Api/UsersSectionsApi.md#updateusersection) | **PUT** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Updates the Section of a user.
*UsersSectionsApi* | [**updateUserSectionBulk**](docs/Api/UsersSectionsApi.md#updateusersectionbulk) | **PUT** /tenants/{tenantId}/users/{userId}/sections/bulk | Updates the Section of a user in bulk.
*V1Api* | [**releaseUserLockout**](docs/Api/V1Api.md#releaseuserlockout) | **PUT** /tenants/{tenantId}/users/{userId}/releaselockout | 
*ValidationResultsAPIApi* | [**findResultsApiJobRunRecordsAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapijobrunrecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/records | Retrieves a list of Job Run Records from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunRuleRecordsAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapijobrunrulerecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/records | Retrieves a list of Job Run Rule Records from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunRulesAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapijobrunrulesasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules | Retrieves a list of Job Run Rules from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunsAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapijobrunsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs | Retrieves a list of Job Runs from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobsAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapijobsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs | Retrieves a list of Jobs from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiRuleSummaries**](docs/Api/ValidationResultsAPIApi.md#findresultsapirulesummaries) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/summary | Retrieves a list Rule Summaries from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiRulesAsync**](docs/Api/ValidationResultsAPIApi.md#findresultsapirulesasync) | **GET** /tenants/{tenantId}/validations/results-api/rules | Retrieves a list of Rules from Validation Results API.
*ValidationResultsAPIApi* | [**getLatestJobRunAsync**](docs/Api/ValidationResultsAPIApi.md#getlatestjobrunasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/latest | Retrieves the latest Job Run from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobById**](docs/Api/ValidationResultsAPIApi.md#getresultsapijobbyid) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId} | Retrieves a Job by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobRunByIdAsync**](docs/Api/ValidationResultsAPIApi.md#getresultsapijobrunbyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId} | Retrieves a Job Run by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobRunRuleByIdAsync**](docs/Api/ValidationResultsAPIApi.md#getresultsapijobrunrulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId} | Retrieves a Job Run Rule by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiRuleByIdAsync**](docs/Api/ValidationResultsAPIApi.md#getresultsapirulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/rules/{ruleId} | Retrieves a Rule by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiRuleSummary**](docs/Api/ValidationResultsAPIApi.md#getresultsapirulesummary) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/summary | Get Rule Summary by ID from the Validation Results API.
*WebhooksApi* | [**createWebhookAsync**](docs/Api/WebhooksApi.md#createwebhookasync) | **POST** /tenants/{tenantId}/webhooks | Creates a new Webhook
*WebhooksApi* | [**deleteWebhookAsync**](docs/Api/WebhooksApi.md#deletewebhookasync) | **DELETE** /tenants/{tenantId}/webhooks/{webhookId} | Removes a webhook.
*WebhooksApi* | [**getAllWebhookSubscriptionsAsync**](docs/Api/WebhooksApi.md#getallwebhooksubscriptionsasync) | **GET** /tenants/{tenantId}/webhooks/events | 
*WebhooksApi* | [**getAllWebhooksAsync**](docs/Api/WebhooksApi.md#getallwebhooksasync) | **GET** /tenants/{tenantId}/webhooks | Retrieves a list of webhooks.
*WebhooksApi* | [**getWebhookByIdAsync**](docs/Api/WebhooksApi.md#getwebhookbyidasync) | **GET** /tenants/{tenantId}/webhooks/{webhookId} | Retrieves a webhook by ID.
*WebhooksApi* | [**requestWebhookReRun**](docs/Api/WebhooksApi.md#requestwebhookrerun) | **POST** /tenants/{tenantId}/webhooks/{webhookId}/dispatches/{dispatchId}/rerun | 
*WebhooksApi* | [**updateWebhookAsync**](docs/Api/WebhooksApi.md#updatewebhookasync) | **PUT** /tenants/{tenantId}/webhooks/{webhookId} | Updates a webhook

## Models

- [AnalyticsApiADLSGen2ConnectorsV1AuthenticationType](docs/Model/AnalyticsApiADLSGen2ConnectorsV1AuthenticationType.md)
- [AnalyticsApiADLSGen2ConnectorsV1ServicePrincipalAuthentication](docs/Model/AnalyticsApiADLSGen2ConnectorsV1ServicePrincipalAuthentication.md)
- [AnalyticsApiCapacitiesV1AnalyticsCapacity](docs/Model/AnalyticsApiCapacitiesV1AnalyticsCapacity.md)
- [AnalyticsApiCapacitiesV1AssignCapacityRequest](docs/Model/AnalyticsApiCapacitiesV1AssignCapacityRequest.md)
- [AnalyticsApiCapacitiesV1CapacityResponse](docs/Model/AnalyticsApiCapacitiesV1CapacityResponse.md)
- [AnalyticsApiCapacitiesV1ResumeCapacityRequest](docs/Model/AnalyticsApiCapacitiesV1ResumeCapacityRequest.md)
- [AnalyticsApiCapacitiesV1SuspendCapacityRequest](docs/Model/AnalyticsApiCapacitiesV1SuspendCapacityRequest.md)
- [AnalyticsApiConfigurationsV1AnalyticsAzureAd](docs/Model/AnalyticsApiConfigurationsV1AnalyticsAzureAd.md)
- [AnalyticsApiConfigurationsV1AnalyticsConfiguration](docs/Model/AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)
- [AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel](docs/Model/AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel.md)
- [AnalyticsApiConfigurationsV1AnalyticsPowerBi](docs/Model/AnalyticsApiConfigurationsV1AnalyticsPowerBi.md)
- [AnalyticsApiConfigurationsV1AnalyticsTriggerOption](docs/Model/AnalyticsApiConfigurationsV1AnalyticsTriggerOption.md)
- [AnalyticsApiConfigurationsV1ConfigurationResponse](docs/Model/AnalyticsApiConfigurationsV1ConfigurationResponse.md)
- [AnalyticsApiConfigurationsV1CreateConfigurationRequest](docs/Model/AnalyticsApiConfigurationsV1CreateConfigurationRequest.md)
- [AnalyticsApiConfigurationsV1HasValidConfigurationResponse](docs/Model/AnalyticsApiConfigurationsV1HasValidConfigurationResponse.md)
- [AnalyticsApiConfigurationsV1TestConnectionResponse](docs/Model/AnalyticsApiConfigurationsV1TestConnectionResponse.md)
- [AnalyticsApiConfigurationsV1UpdateConfigurationRequest](docs/Model/AnalyticsApiConfigurationsV1UpdateConfigurationRequest.md)
- [AnalyticsApiConnectorsV1ConnectorDeletedResponse](docs/Model/AnalyticsApiConnectorsV1ConnectorDeletedResponse.md)
- [AnalyticsApiGroupsV1AddGroupUsersRequest](docs/Model/AnalyticsApiGroupsV1AddGroupUsersRequest.md)
- [AnalyticsApiGroupsV1AnalyticsGroupUser](docs/Model/AnalyticsApiGroupsV1AnalyticsGroupUser.md)
- [AnalyticsApiGroupsV1CreateGroupRequest](docs/Model/AnalyticsApiGroupsV1CreateGroupRequest.md)
- [AnalyticsApiGroupsV1GroupResponse](docs/Model/AnalyticsApiGroupsV1GroupResponse.md)
- [AnalyticsApiGroupsV1GroupUsersResponse](docs/Model/AnalyticsApiGroupsV1GroupUsersResponse.md)
- [AnalyticsApiGroupsV1GroupsResponse](docs/Model/AnalyticsApiGroupsV1GroupsResponse.md)
- [AnalyticsApiLakehousesV1LakehouseRecord](docs/Model/AnalyticsApiLakehousesV1LakehouseRecord.md)
- [AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse](docs/Model/AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse.md)
- [AnalyticsApiReportsV1AnalyticsEmbedToken](docs/Model/AnalyticsApiReportsV1AnalyticsEmbedToken.md)
- [AnalyticsApiReportsV1AnalyticsReport](docs/Model/AnalyticsApiReportsV1AnalyticsReport.md)
- [AnalyticsApiReportsV1AnalyticsReportDataset](docs/Model/AnalyticsApiReportsV1AnalyticsReportDataset.md)
- [AnalyticsApiReportsV1DownloadReportResponse](docs/Model/AnalyticsApiReportsV1DownloadReportResponse.md)
- [AnalyticsApiReportsV1ReportIdResponse](docs/Model/AnalyticsApiReportsV1ReportIdResponse.md)
- [AnalyticsApiReportsV1ReportPaginatedItemsResponse](docs/Model/AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)
- [AnalyticsApiReportsV1ReportPreferenceDetailsResponse](docs/Model/AnalyticsApiReportsV1ReportPreferenceDetailsResponse.md)
- [AnalyticsApiReportsV1ReportPreferencesResponse](docs/Model/AnalyticsApiReportsV1ReportPreferencesResponse.md)
- [AnalyticsApiReportsV1ReportPreferencesSavedResponse](docs/Model/AnalyticsApiReportsV1ReportPreferencesSavedResponse.md)
- [AnalyticsApiReportsV1ReportResponse](docs/Model/AnalyticsApiReportsV1ReportResponse.md)
- [AnalyticsApiReportsV1ReportSource](docs/Model/AnalyticsApiReportsV1ReportSource.md)
- [AnalyticsApiReportsV1SyncLatestVersionRequest](docs/Model/AnalyticsApiReportsV1SyncLatestVersionRequest.md)
- [AnalyticsApiReportsV1SyncWorkspacesRequest](docs/Model/AnalyticsApiReportsV1SyncWorkspacesRequest.md)
- [AnalyticsApiUserAuthorizationsV1SchoolYear](docs/Model/AnalyticsApiUserAuthorizationsV1SchoolYear.md)
- [AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse](docs/Model/AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse.md)
- [AnalyticsApiUserAuthorizationsV1UserAuthorizationsListResponse](docs/Model/AnalyticsApiUserAuthorizationsV1UserAuthorizationsListResponse.md)
- [AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse](docs/Model/AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse.md)
- [ApplicationApiApplicationV1ApplicationListResponse](docs/Model/ApplicationApiApplicationV1ApplicationListResponse.md)
- [ApplicationApiApplicationV1ApplicationProfileResponse](docs/Model/ApplicationApiApplicationV1ApplicationProfileResponse.md)
- [ApplicationApiApplicationV1ApplicationStatus](docs/Model/ApplicationApiApplicationV1ApplicationStatus.md)
- [ApplicationApiApplicationV1ApplicationSubscriptionType](docs/Model/ApplicationApiApplicationV1ApplicationSubscriptionType.md)
- [ApplicationApiApplicationV1ApplicationType](docs/Model/ApplicationApiApplicationV1ApplicationType.md)
- [ApplicationApiApplicationV1PaginatedItemsResponse](docs/Model/ApplicationApiApplicationV1PaginatedItemsResponse.md)
- [ApplicationApiApplicationV1Role](docs/Model/ApplicationApiApplicationV1Role.md)
- [ApplicationApiApplicationV1UrlType](docs/Model/ApplicationApiApplicationV1UrlType.md)
- [ChangeLogChangeV1ChangeLogResponse](docs/Model/ChangeLogChangeV1ChangeLogResponse.md)
- [ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel](docs/Model/ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel.md)
- [DataSyncApiConnectionV1ConnectionListResponse](docs/Model/DataSyncApiConnectionV1ConnectionListResponse.md)
- [DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel](docs/Model/DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel.md)
- [DataSyncApiConnectionV1ConnectionMetadata](docs/Model/DataSyncApiConnectionV1ConnectionMetadata.md)
- [DataSyncApiConnectionV1ConnectionProfileResponse](docs/Model/DataSyncApiConnectionV1ConnectionProfileResponse.md)
- [DataSyncApiConnectionV1ConnectionTestedResponse](docs/Model/DataSyncApiConnectionV1ConnectionTestedResponse.md)
- [DataSyncApiConnectionV1TestConnectionRequest](docs/Model/DataSyncApiConnectionV1TestConnectionRequest.md)
- [DataSyncApiDslV1CreateJobRequest](docs/Model/DataSyncApiDslV1CreateJobRequest.md)
- [DataSyncApiDslV1DslJobExecutedResponse](docs/Model/DataSyncApiDslV1DslJobExecutedResponse.md)
- [DataSyncApiDslV1DslProfile](docs/Model/DataSyncApiDslV1DslProfile.md)
- [DataSyncApiDslV1JobCreatedResponse](docs/Model/DataSyncApiDslV1JobCreatedResponse.md)
- [DataSyncApiDslV1UpdateJobRequest](docs/Model/DataSyncApiDslV1UpdateJobRequest.md)
- [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobMode](docs/Model/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobMode.md)
- [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile](docs/Model/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile.md)
- [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProvider](docs/Model/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProvider.md)
- [DataSyncApiEdFiRosterSyncV1UseSSAInsteadOfSEOAAOptions](docs/Model/DataSyncApiEdFiRosterSyncV1UseSSAInsteadOfSEOAAOptions.md)
- [DataSyncApiJobExecutionLogV1JobExecutionLogEntry](docs/Model/DataSyncApiJobExecutionLogV1JobExecutionLogEntry.md)
- [DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel](docs/Model/DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel.md)
- [DataSyncApiJobExecutionLogV1MessageType](docs/Model/DataSyncApiJobExecutionLogV1MessageType.md)
- [DataSyncApiJobExecutionV1ChildJob](docs/Model/DataSyncApiJobExecutionV1ChildJob.md)
- [DataSyncApiJobExecutionV1JobExecutionListResponse](docs/Model/DataSyncApiJobExecutionV1JobExecutionListResponse.md)
- [DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel](docs/Model/DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel.md)
- [DataSyncApiJobExecutionV1JobExecutionStatus](docs/Model/DataSyncApiJobExecutionV1JobExecutionStatus.md)
- [DataSyncApiJobExecutionV1Metric](docs/Model/DataSyncApiJobExecutionV1Metric.md)
- [DataSyncApiJobTypeV1JobMetadataField](docs/Model/DataSyncApiJobTypeV1JobMetadataField.md)
- [DataSyncApiJobTypeV1JobTypeListResponse](docs/Model/DataSyncApiJobTypeV1JobTypeListResponse.md)
- [DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel](docs/Model/DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel.md)
- [DataSyncApiJobTypeV1JobTypeProfileResponse](docs/Model/DataSyncApiJobTypeV1JobTypeProfileResponse.md)
- [DataSyncApiJobTypeV1Profile](docs/Model/DataSyncApiJobTypeV1Profile.md)
- [DataSyncApiJobV1ActivateJobRequest](docs/Model/DataSyncApiJobV1ActivateJobRequest.md)
- [DataSyncApiJobV1CancelJobRequest](docs/Model/DataSyncApiJobV1CancelJobRequest.md)
- [DataSyncApiJobV1ChildJob](docs/Model/DataSyncApiJobV1ChildJob.md)
- [DataSyncApiJobV1DataRefreshType](docs/Model/DataSyncApiJobV1DataRefreshType.md)
- [DataSyncApiJobV1DeactivateJobRequest](docs/Model/DataSyncApiJobV1DeactivateJobRequest.md)
- [DataSyncApiJobV1ExecuteJobRequest](docs/Model/DataSyncApiJobV1ExecuteJobRequest.md)
- [DataSyncApiJobV1JobExecutionMetadata](docs/Model/DataSyncApiJobV1JobExecutionMetadata.md)
- [DataSyncApiJobV1JobExecutionRequestedResponse](docs/Model/DataSyncApiJobV1JobExecutionRequestedResponse.md)
- [DataSyncApiJobV1JobExecutionStatus](docs/Model/DataSyncApiJobV1JobExecutionStatus.md)
- [DataSyncApiJobV1JobListResponse](docs/Model/DataSyncApiJobV1JobListResponse.md)
- [DataSyncApiJobV1JobListResponsePaginatedItemsViewModel](docs/Model/DataSyncApiJobV1JobListResponsePaginatedItemsViewModel.md)
- [DataSyncApiJobV1JobMetadata](docs/Model/DataSyncApiJobV1JobMetadata.md)
- [DataSyncApiJobV1JobProfileResponse](docs/Model/DataSyncApiJobV1JobProfileResponse.md)
- [DataSyncApiJobV1JobStatus](docs/Model/DataSyncApiJobV1JobStatus.md)
- [DataSyncApiJobV1Metric](docs/Model/DataSyncApiJobV1Metric.md)
- [DataSyncApiJobV1Schedule](docs/Model/DataSyncApiJobV1Schedule.md)
- [DataSyncApiProviderV1ConnectionMetadataField](docs/Model/DataSyncApiProviderV1ConnectionMetadataField.md)
- [DataSyncApiProviderV1ConnectionType](docs/Model/DataSyncApiProviderV1ConnectionType.md)
- [DataSyncApiProviderV1ProviderListResponse](docs/Model/DataSyncApiProviderV1ProviderListResponse.md)
- [DataSyncApiProviderV1ProviderListResponsePaginatedItemsViewModel](docs/Model/DataSyncApiProviderV1ProviderListResponsePaginatedItemsViewModel.md)
- [DataSyncApiProviderV1ProviderProfileResponse](docs/Model/DataSyncApiProviderV1ProviderProfileResponse.md)
- [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile](docs/Model/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile.md)
- [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncJobExecutedResponse](docs/Model/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncJobExecutedResponse.md)
- [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile](docs/Model/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile.md)
- [EdFiAdminApiApplicationAccessV1ApplicationAccessResponse](docs/Model/EdFiAdminApiApplicationAccessV1ApplicationAccessResponse.md)
- [EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel](docs/Model/EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel.md)
- [EdFiAdminApiApplicationAccessV1ApplicationUserAccessResponse](docs/Model/EdFiAdminApiApplicationAccessV1ApplicationUserAccessResponse.md)
- [EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest](docs/Model/EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest.md)
- [EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest](docs/Model/EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest.md)
- [EdGraphCommonErrorsCoreProblemDetails](docs/Model/EdGraphCommonErrorsCoreProblemDetails.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsConnectionMetadata](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsConnectionMetadata.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionValidationRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionValidationRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionValidationRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionValidationRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsDataRefreshType](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsDataRefreshType.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobCategory](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobCategory.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobMetadata](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobMetadata.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsSchedule](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsSchedule.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterClaimDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterClaimDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantAdditionalSetting](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantAdditionalSetting.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderId](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderId.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderStatus](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderStatus.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviders](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviders.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantSetting](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantSetting.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserResponse](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserResponse.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserSearchStatus](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserSearchStatus.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffResponse](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffResponse.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchStatus](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchStatus.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionValidationResponseDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionValidationResponseDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityConditionDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityConditionDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityRuleDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityRuleDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesRole](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesRole.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponse](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponse.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsLatestRunDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsLatestRunDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicense](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicense.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseRole](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseRole.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResult](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResult.md)
- [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk](docs/Model/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfilePipelineDTO](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfilePipelineDTO.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesMappedConnectorListResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesMappedConnectorListResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLog](docs/Model/EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLog.md)
- [EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto](docs/Model/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto.md)
- [EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult](docs/Model/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult.md)
- [EdGraphHttpAggregatorsTenantApiServicesFormsV1Form](docs/Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1Form.md)
- [EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceConfiguration](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceConfiguration.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceRole](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceRole.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertReportPreferenceDetails](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertReportPreferenceDetails.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApi](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApi.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiDataModel](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiDataModel.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUrls](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUrls.md)
- [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult](docs/Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult.md)
- [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)
- [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest](docs/Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationRole](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationRole.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTileResponseWithUserApplicationLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTileResponseWithUserApplicationLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationUrl](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationUrl.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesTenantStatus](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesTenantStatus.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantEducationOrganizationResponse](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantEducationOrganizationResponse.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantResponse](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantResponse.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLogin](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLogin.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfilePreference](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfilePreference.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenant](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenant.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicense](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicense.md)
- [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicenseRole](docs/Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicenseRole.md)
- [EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest](docs/Model/EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest.md)
- [EdGraphServicesStateReportingV1AddSubmissionMetricsRequest](docs/Model/EdGraphServicesStateReportingV1AddSubmissionMetricsRequest.md)
- [EdGraphServicesStateReportingV1Category](docs/Model/EdGraphServicesStateReportingV1Category.md)
- [EdGraphServicesStateReportingV1CreateEnvironmentRequest](docs/Model/EdGraphServicesStateReportingV1CreateEnvironmentRequest.md)
- [EdGraphServicesStateReportingV1CreateReportingPeriodRequest](docs/Model/EdGraphServicesStateReportingV1CreateReportingPeriodRequest.md)
- [EdGraphServicesStateReportingV1DataUser](docs/Model/EdGraphServicesStateReportingV1DataUser.md)
- [EdGraphServicesStateReportingV1EnvironmentCreatedResponse](docs/Model/EdGraphServicesStateReportingV1EnvironmentCreatedResponse.md)
- [EdGraphServicesStateReportingV1EnvironmentDeletedResponse](docs/Model/EdGraphServicesStateReportingV1EnvironmentDeletedResponse.md)
- [EdGraphServicesStateReportingV1EnvironmentListResponse](docs/Model/EdGraphServicesStateReportingV1EnvironmentListResponse.md)
- [EdGraphServicesStateReportingV1EnvironmentProfileResponse](docs/Model/EdGraphServicesStateReportingV1EnvironmentProfileResponse.md)
- [EdGraphServicesStateReportingV1EnvironmentUpdatedResponse](docs/Model/EdGraphServicesStateReportingV1EnvironmentUpdatedResponse.md)
- [EdGraphServicesStateReportingV1PaginatedCategories](docs/Model/EdGraphServicesStateReportingV1PaginatedCategories.md)
- [EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse](docs/Model/EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse.md)
- [EdGraphServicesStateReportingV1PaginatedRecords](docs/Model/EdGraphServicesStateReportingV1PaginatedRecords.md)
- [EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecords](docs/Model/EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecords.md)
- [EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule](docs/Model/EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule.md)
- [EdGraphServicesStateReportingV1PaginatedReportingPeriods](docs/Model/EdGraphServicesStateReportingV1PaginatedReportingPeriods.md)
- [EdGraphServicesStateReportingV1PaginatedRuleRecords](docs/Model/EdGraphServicesStateReportingV1PaginatedRuleRecords.md)
- [EdGraphServicesStateReportingV1PaginatedSubCategories](docs/Model/EdGraphServicesStateReportingV1PaginatedSubCategories.md)
- [EdGraphServicesStateReportingV1PaginatedSubmissionLogs](docs/Model/EdGraphServicesStateReportingV1PaginatedSubmissionLogs.md)
- [EdGraphServicesStateReportingV1PaginatedSubmissions](docs/Model/EdGraphServicesStateReportingV1PaginatedSubmissions.md)
- [EdGraphServicesStateReportingV1PipelineRun](docs/Model/EdGraphServicesStateReportingV1PipelineRun.md)
- [EdGraphServicesStateReportingV1PostReportingPeriodRequest](docs/Model/EdGraphServicesStateReportingV1PostReportingPeriodRequest.md)
- [EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus.md)
- [EdGraphServicesStateReportingV1ReportingPeriodCertificationStatusCategory](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodCertificationStatusCategory.md)
- [EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodListResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodListResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodPostedResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodPostedResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodProfileResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodProfileResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodRunResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodRunResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodStep](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodStep.md)
- [EdGraphServicesStateReportingV1ReportingPeriodStepStatus](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodStepStatus.md)
- [EdGraphServicesStateReportingV1ReportingPeriodToggledResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodToggledResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodValidationSummary](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodValidationSummary.md)
- [EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId.md)
- [EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse.md)
- [EdGraphServicesStateReportingV1ReportingPeriodValidationsRunDto](docs/Model/EdGraphServicesStateReportingV1ReportingPeriodValidationsRunDto.md)
- [EdGraphServicesStateReportingV1Rule](docs/Model/EdGraphServicesStateReportingV1Rule.md)
- [EdGraphServicesStateReportingV1RunReportingPeriodRequest](docs/Model/EdGraphServicesStateReportingV1RunReportingPeriodRequest.md)
- [EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest](docs/Model/EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest.md)
- [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest](docs/Model/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest.md)
- [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequestTypesRecord](docs/Model/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequestTypesRecord.md)
- [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest](docs/Model/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest.md)
- [EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest](docs/Model/EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest.md)
- [EdGraphServicesStateReportingV1SetSubmissionStatusRequest](docs/Model/EdGraphServicesStateReportingV1SetSubmissionStatusRequest.md)
- [EdGraphServicesStateReportingV1SubCategory](docs/Model/EdGraphServicesStateReportingV1SubCategory.md)
- [EdGraphServicesStateReportingV1SubmissionCancelledResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionCancelledResponse.md)
- [EdGraphServicesStateReportingV1SubmissionListResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionListResponse.md)
- [EdGraphServicesStateReportingV1SubmissionLog](docs/Model/EdGraphServicesStateReportingV1SubmissionLog.md)
- [EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse.md)
- [EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse.md)
- [EdGraphServicesStateReportingV1SubmissionMetricsDetails](docs/Model/EdGraphServicesStateReportingV1SubmissionMetricsDetails.md)
- [EdGraphServicesStateReportingV1SubmissionMetricsResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionMetricsResponse.md)
- [EdGraphServicesStateReportingV1SubmissionProfile](docs/Model/EdGraphServicesStateReportingV1SubmissionProfile.md)
- [EdGraphServicesStateReportingV1SubmissionStatus](docs/Model/EdGraphServicesStateReportingV1SubmissionStatus.md)
- [EdGraphServicesStateReportingV1SubmissionStatusSetResponse](docs/Model/EdGraphServicesStateReportingV1SubmissionStatusSetResponse.md)
- [EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest](docs/Model/EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest.md)
- [EdGraphServicesStateReportingV1UpdateEnvironmentRequest](docs/Model/EdGraphServicesStateReportingV1UpdateEnvironmentRequest.md)
- [EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest](docs/Model/EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest.md)
- [EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequestTypesReportingPeriod](docs/Model/EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequestTypesReportingPeriod.md)
- [EdGraphServicesStateReportingV1UpdateReportingPeriodRequest](docs/Model/EdGraphServicesStateReportingV1UpdateReportingPeriodRequest.md)
- [EdGraphServicesStateReportingV1ValidationResultRecord](docs/Model/EdGraphServicesStateReportingV1ValidationResultRecord.md)
- [EdGraphServicesStateReportingV1ValidationSummaryCategory](docs/Model/EdGraphServicesStateReportingV1ValidationSummaryCategory.md)
- [EdGraphServicesStateReportingV1ValidationSummarySubCategory](docs/Model/EdGraphServicesStateReportingV1ValidationSummarySubCategory.md)
- [EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest](docs/Model/EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest.md)
- [EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse](docs/Model/EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse.md)
- [EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest](docs/Model/EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest.md)
- [EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry](docs/Model/EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry.md)
- [EdfiAdminApiEdfiAdminV1AddSchoolYearRequest](docs/Model/EdfiAdminApiEdfiAdminV1AddSchoolYearRequest.md)
- [EdfiAdminApiEdfiAdminV1ApplicationEndpoint](docs/Model/EdfiAdminApiEdfiAdminV1ApplicationEndpoint.md)
- [EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse](docs/Model/EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse.md)
- [EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest](docs/Model/EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest.md)
- [EdfiAdminApiEdfiAdminV1ClaimSet](docs/Model/EdfiAdminApiEdfiAdminV1ClaimSet.md)
- [EdfiAdminApiEdfiAdminV1ClaimSetDetailsResourceClaim](docs/Model/EdfiAdminApiEdfiAdminV1ClaimSetDetailsResourceClaim.md)
- [EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1CloneInstanceRequest](docs/Model/EdfiAdminApiEdfiAdminV1CloneInstanceRequest.md)
- [EdfiAdminApiEdfiAdminV1CloneInstanceResponse](docs/Model/EdfiAdminApiEdfiAdminV1CloneInstanceResponse.md)
- [EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateInstanceRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateInstanceRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateInstanceRequestSchoolYear](docs/Model/EdfiAdminApiEdfiAdminV1CreateInstanceRequestSchoolYear.md)
- [EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest.md)
- [EdfiAdminApiEdfiAdminV1CreateVendorRequest](docs/Model/EdfiAdminApiEdfiAdminV1CreateVendorRequest.md)
- [EdfiAdminApiEdfiAdminV1DatabaseTier](docs/Model/EdfiAdminApiEdfiAdminV1DatabaseTier.md)
- [EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorMapping](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorMapping.md)
- [EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorMappingModelEntity](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorMappingModelEntity.md)
- [EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorType](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorType.md)
- [EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse](docs/Model/EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplication](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplication.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationListResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationListResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnection](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnection.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionListModel](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionListModel.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionTier](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionTier.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionTierListModel](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionTierListModel.md)
- [EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptor](docs/Model/EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptor.md)
- [EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse](docs/Model/EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse.md)
- [EdfiAdminApiEdfiAdminV1EducationOrganization](docs/Model/EdfiAdminApiEdfiAdminV1EducationOrganization.md)
- [EdfiAdminApiEdfiAdminV1EducationOrganizationAddress](docs/Model/EdfiAdminApiEdfiAdminV1EducationOrganizationAddress.md)
- [EdfiAdminApiEdfiAdminV1EducationOrganizationCategoryDescriptor](docs/Model/EdfiAdminApiEdfiAdminV1EducationOrganizationCategoryDescriptor.md)
- [EdfiAdminApiEdfiAdminV1EducationServiceCenter](docs/Model/EdfiAdminApiEdfiAdminV1EducationServiceCenter.md)
- [EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1GenderRepresentation](docs/Model/EdfiAdminApiEdfiAdminV1GenderRepresentation.md)
- [EdfiAdminApiEdfiAdminV1GenerateReportsResponse](docs/Model/EdfiAdminApiEdfiAdminV1GenerateReportsResponse.md)
- [EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse](docs/Model/EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse.md)
- [EdfiAdminApiEdfiAdminV1Instance](docs/Model/EdfiAdminApiEdfiAdminV1Instance.md)
- [EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApiClientListResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApiClientListResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1InstanceDatabase](docs/Model/EdfiAdminApiEdfiAdminV1InstanceDatabase.md)
- [EdfiAdminApiEdfiAdminV1InstanceDatabaseJobs](docs/Model/EdfiAdminApiEdfiAdminV1InstanceDatabaseJobs.md)
- [EdfiAdminApiEdfiAdminV1InstanceDatabases](docs/Model/EdfiAdminApiEdfiAdminV1InstanceDatabases.md)
- [EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceListModel](docs/Model/EdfiAdminApiEdfiAdminV1InstanceListModel.md)
- [EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1InstanceOdsDatabase](docs/Model/EdfiAdminApiEdfiAdminV1InstanceOdsDatabase.md)
- [EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponse.md)
- [EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1InstanceType](docs/Model/EdfiAdminApiEdfiAdminV1InstanceType.md)
- [EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)
- [EdfiAdminApiEdfiAdminV1LocalEducationAgency](docs/Model/EdfiAdminApiEdfiAdminV1LocalEducationAgency.md)
- [EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponse](docs/Model/EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponse.md)
- [EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1OdsApiConnectionEndpoint](docs/Model/EdfiAdminApiEdfiAdminV1OdsApiConnectionEndpoint.md)
- [EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApi](docs/Model/EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApi.md)
- [EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApiDataModel](docs/Model/EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApiDataModel.md)
- [EdfiAdminApiEdfiAdminV1Onboarding](docs/Model/EdfiAdminApiEdfiAdminV1Onboarding.md)
- [EdfiAdminApiEdfiAdminV1OnboardingStep](docs/Model/EdfiAdminApiEdfiAdminV1OnboardingStep.md)
- [EdfiAdminApiEdfiAdminV1RaceRepresentation](docs/Model/EdfiAdminApiEdfiAdminV1RaceRepresentation.md)
- [EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse](docs/Model/EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)
- [EdfiAdminApiEdfiAdminV1RelatedInstance](docs/Model/EdfiAdminApiEdfiAdminV1RelatedInstance.md)
- [EdfiAdminApiEdfiAdminV1ReportsStatusResponse](docs/Model/EdfiAdminApiEdfiAdminV1ReportsStatusResponse.md)
- [EdfiAdminApiEdfiAdminV1ResetInstanceResponse](docs/Model/EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)
- [EdfiAdminApiEdfiAdminV1ResourceClaim](docs/Model/EdfiAdminApiEdfiAdminV1ResourceClaim.md)
- [EdfiAdminApiEdfiAdminV1SaveClaimSetRequest](docs/Model/EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md)
- [EdfiAdminApiEdfiAdminV1SaveClaimSetResponse](docs/Model/EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)
- [EdfiAdminApiEdfiAdminV1SchoolCountRepresentation](docs/Model/EdfiAdminApiEdfiAdminV1SchoolCountRepresentation.md)
- [EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse.md)
- [EdfiAdminApiEdfiAdminV1SecretEncryptionMetadata](docs/Model/EdfiAdminApiEdfiAdminV1SecretEncryptionMetadata.md)
- [EdfiAdminApiEdfiAdminV1SecretValueType](docs/Model/EdfiAdminApiEdfiAdminV1SecretValueType.md)
- [EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest](docs/Model/EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest.md)
- [EdfiAdminApiEdfiAdminV1StateEducationAgency](docs/Model/EdfiAdminApiEdfiAdminV1StateEducationAgency.md)
- [EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse.md)
- [EdfiAdminApiEdfiAdminV1StudentEconomicSituationRepresentation](docs/Model/EdfiAdminApiEdfiAdminV1StudentEconomicSituationRepresentation.md)
- [EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse.md)
- [EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse.md)
- [EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse.md)
- [EdfiAdminApiEdfiAdminV1StudentProgramRepresentation](docs/Model/EdfiAdminApiEdfiAdminV1StudentProgramRepresentation.md)
- [EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse.md)
- [EdfiAdminApiEdfiAdminV1SyncApplicationRequest](docs/Model/EdfiAdminApiEdfiAdminV1SyncApplicationRequest.md)
- [EdfiAdminApiEdfiAdminV1SyncClaimSetRequest](docs/Model/EdfiAdminApiEdfiAdminV1SyncClaimSetRequest.md)
- [EdfiAdminApiEdfiAdminV1SyncEntry](docs/Model/EdfiAdminApiEdfiAdminV1SyncEntry.md)
- [EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest](docs/Model/EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest.md)
- [EdfiAdminApiEdfiAdminV1SyncResponse](docs/Model/EdfiAdminApiEdfiAdminV1SyncResponse.md)
- [EdfiAdminApiEdfiAdminV1SyncVendorRequest](docs/Model/EdfiAdminApiEdfiAdminV1SyncVendorRequest.md)
- [EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest](docs/Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md)
- [EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse](docs/Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)
- [EdfiAdminApiEdfiAdminV1TierOdsApiConnection](docs/Model/EdfiAdminApiEdfiAdminV1TierOdsApiConnection.md)
- [EdfiAdminApiEdfiAdminV1TierOdsApiConnectionListModel](docs/Model/EdfiAdminApiEdfiAdminV1TierOdsApiConnectionListModel.md)
- [EdfiAdminApiEdfiAdminV1TierSqlConnection](docs/Model/EdfiAdminApiEdfiAdminV1TierSqlConnection.md)
- [EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse](docs/Model/EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse.md)
- [EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateInstanceRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateInstanceRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest.md)
- [EdfiAdminApiEdfiAdminV1UpdateVendorRequest](docs/Model/EdfiAdminApiEdfiAdminV1UpdateVendorRequest.md)
- [EdfiAdminApiEdfiAdminV1Vendor](docs/Model/EdfiAdminApiEdfiAdminV1Vendor.md)
- [EdfiAdminApiEdfiAdminV1VendorCreatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1VendorCreatedResponse.md)
- [EdfiAdminApiEdfiAdminV1VendorListResponse](docs/Model/EdfiAdminApiEdfiAdminV1VendorListResponse.md)
- [EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel](docs/Model/EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel.md)
- [EdfiAdminApiEdfiAdminV1VendorProfileResponse](docs/Model/EdfiAdminApiEdfiAdminV1VendorProfileResponse.md)
- [EdfiAdminApiEdfiAdminV1VendorUpdatedResponse](docs/Model/EdfiAdminApiEdfiAdminV1VendorUpdatedResponse.md)
- [EvaluationApiEvaluationSettingsV1ApplicationSetResponse](docs/Model/EvaluationApiEvaluationSettingsV1ApplicationSetResponse.md)
- [EvaluationApiEvaluationSettingsV1EvaluationSettingResponse](docs/Model/EvaluationApiEvaluationSettingsV1EvaluationSettingResponse.md)
- [EvaluationApiEvaluationSettingsV1FormConfigurationResponse](docs/Model/EvaluationApiEvaluationSettingsV1FormConfigurationResponse.md)
- [EvaluationApiEvaluationSettingsV1FormVersionConfigurationResponse](docs/Model/EvaluationApiEvaluationSettingsV1FormVersionConfigurationResponse.md)
- [EvaluationApiEvaluationSettingsV1PersonaResponse](docs/Model/EvaluationApiEvaluationSettingsV1PersonaResponse.md)
- [EvaluationApiEvaluationSettingsV1RoleConfigurationResponse](docs/Model/EvaluationApiEvaluationSettingsV1RoleConfigurationResponse.md)
- [EvaluationApiEvaluationSettingsV1ScheduleType](docs/Model/EvaluationApiEvaluationSettingsV1ScheduleType.md)
- [EvaluationApiEvaluationSettingsV1SetApplicationRequest](docs/Model/EvaluationApiEvaluationSettingsV1SetApplicationRequest.md)
- [EvaluationApiEvaluationSettingsV1SetFormConfigurationRequest](docs/Model/EvaluationApiEvaluationSettingsV1SetFormConfigurationRequest.md)
- [EvaluationApiEvaluationSettingsV1SetFormVersionConfigurationRequest](docs/Model/EvaluationApiEvaluationSettingsV1SetFormVersionConfigurationRequest.md)
- [EvaluationApiEvaluationSettingsV1SetUsersRequest](docs/Model/EvaluationApiEvaluationSettingsV1SetUsersRequest.md)
- [EvaluationApiEvaluationSettingsV1UsersSetResponse](docs/Model/EvaluationApiEvaluationSettingsV1UsersSetResponse.md)
- [EvaluationApiEvaluationsV1CampusResponse](docs/Model/EvaluationApiEvaluationsV1CampusResponse.md)
- [EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel](docs/Model/EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel.md)
- [EvaluationApiEvaluationsV1CreateEvaluationRequest](docs/Model/EvaluationApiEvaluationsV1CreateEvaluationRequest.md)
- [EvaluationApiEvaluationsV1EvaluationCountResponse](docs/Model/EvaluationApiEvaluationsV1EvaluationCountResponse.md)
- [EvaluationApiEvaluationsV1EvaluationCreatedResponse](docs/Model/EvaluationApiEvaluationsV1EvaluationCreatedResponse.md)
- [EvaluationApiEvaluationsV1EvaluationDeletedResponse](docs/Model/EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)
- [EvaluationApiEvaluationsV1EvaluationResponse](docs/Model/EvaluationApiEvaluationsV1EvaluationResponse.md)
- [EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel](docs/Model/EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel.md)
- [EvaluationApiEvaluationsV1EvaluationStatus](docs/Model/EvaluationApiEvaluationsV1EvaluationStatus.md)
- [EvaluationApiEvaluationsV1EvaluationUpdatedResponse](docs/Model/EvaluationApiEvaluationsV1EvaluationUpdatedResponse.md)
- [EvaluationApiEvaluationsV1FormResponse](docs/Model/EvaluationApiEvaluationsV1FormResponse.md)
- [EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel](docs/Model/EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel.md)
- [EvaluationApiEvaluationsV1OrganizationDiscriminator](docs/Model/EvaluationApiEvaluationsV1OrganizationDiscriminator.md)
- [EvaluationApiEvaluationsV1OrganizationIdentifierType](docs/Model/EvaluationApiEvaluationsV1OrganizationIdentifierType.md)
- [EvaluationApiEvaluationsV1UpdateEvaluationRequest](docs/Model/EvaluationApiEvaluationsV1UpdateEvaluationRequest.md)
- [FormApiFormComponentsV1FormComponentResponse](docs/Model/FormApiFormComponentsV1FormComponentResponse.md)
- [FormApiFormComponentsV1FormComponentResponsePaginatedItemsViewModel](docs/Model/FormApiFormComponentsV1FormComponentResponsePaginatedItemsViewModel.md)
- [FormApiFormComponentsV1FormComponentType](docs/Model/FormApiFormComponentsV1FormComponentType.md)
- [FormApiFormsV1AudienceType](docs/Model/FormApiFormsV1AudienceType.md)
- [FormApiFormsV1CreateFormRequest](docs/Model/FormApiFormsV1CreateFormRequest.md)
- [FormApiFormsV1CreateFullFormRequest](docs/Model/FormApiFormsV1CreateFullFormRequest.md)
- [FormApiFormsV1CreateFullQuestionRequest](docs/Model/FormApiFormsV1CreateFullQuestionRequest.md)
- [FormApiFormsV1CreateFullQuestionValidationRequest](docs/Model/FormApiFormsV1CreateFullQuestionValidationRequest.md)
- [FormApiFormsV1CreateFullSectionRequest](docs/Model/FormApiFormsV1CreateFullSectionRequest.md)
- [FormApiFormsV1FormAccessResponse](docs/Model/FormApiFormsV1FormAccessResponse.md)
- [FormApiFormsV1FormAccessSetResponse](docs/Model/FormApiFormsV1FormAccessSetResponse.md)
- [FormApiFormsV1FormCreatedResponse](docs/Model/FormApiFormsV1FormCreatedResponse.md)
- [FormApiFormsV1FormDeletedResponse](docs/Model/FormApiFormsV1FormDeletedResponse.md)
- [FormApiFormsV1FormDuplicatedResponse](docs/Model/FormApiFormsV1FormDuplicatedResponse.md)
- [FormApiFormsV1FormSource](docs/Model/FormApiFormsV1FormSource.md)
- [FormApiFormsV1FormStatus](docs/Model/FormApiFormsV1FormStatus.md)
- [FormApiFormsV1FormUpdatedResponse](docs/Model/FormApiFormsV1FormUpdatedResponse.md)
- [FormApiFormsV1FullFormCreatedResponse](docs/Model/FormApiFormsV1FullFormCreatedResponse.md)
- [FormApiFormsV1FullFormSchemaResponse](docs/Model/FormApiFormsV1FullFormSchemaResponse.md)
- [FormApiFormsV1FullFormUpdatedResponse](docs/Model/FormApiFormsV1FullFormUpdatedResponse.md)
- [FormApiFormsV1SchemaStatus](docs/Model/FormApiFormsV1SchemaStatus.md)
- [FormApiFormsV1SetFormAccessRequest](docs/Model/FormApiFormsV1SetFormAccessRequest.md)
- [FormApiFormsV1UpdateFormRequest](docs/Model/FormApiFormsV1UpdateFormRequest.md)
- [FormApiFormsV1UpdateFullFormRequest](docs/Model/FormApiFormsV1UpdateFullFormRequest.md)
- [FormApiFormsV1UpdateFullQuestionRequest](docs/Model/FormApiFormsV1UpdateFullQuestionRequest.md)
- [FormApiFormsV1UpdateFullQuestionValidationRequest](docs/Model/FormApiFormsV1UpdateFullQuestionValidationRequest.md)
- [FormApiFormsV1UpdateFullSectionRequest](docs/Model/FormApiFormsV1UpdateFullSectionRequest.md)
- [FormApiQuestionsV1QuestionCreatedResponse](docs/Model/FormApiQuestionsV1QuestionCreatedResponse.md)
- [FormApiQuestionsV1QuestionDeletedResponse](docs/Model/FormApiQuestionsV1QuestionDeletedResponse.md)
- [FormApiQuestionsV1QuestionType](docs/Model/FormApiQuestionsV1QuestionType.md)
- [FormApiQuestionsV1QuestionUpdatedResponse](docs/Model/FormApiQuestionsV1QuestionUpdatedResponse.md)
- [FormApiQuestionsV1QuestionVisibilityCondition](docs/Model/FormApiQuestionsV1QuestionVisibilityCondition.md)
- [FormApiQuestionsV1QuestionVisibilityRule](docs/Model/FormApiQuestionsV1QuestionVisibilityRule.md)
- [FormApiSectionsV1CreateSectionRequest](docs/Model/FormApiSectionsV1CreateSectionRequest.md)
- [FormApiSectionsV1SectionCreatedResponse](docs/Model/FormApiSectionsV1SectionCreatedResponse.md)
- [FormApiSectionsV1SectionDeletedResponse](docs/Model/FormApiSectionsV1SectionDeletedResponse.md)
- [FormApiSectionsV1SectionResponse](docs/Model/FormApiSectionsV1SectionResponse.md)
- [FormApiSectionsV1SectionResponsePaginatedItemsViewModel](docs/Model/FormApiSectionsV1SectionResponsePaginatedItemsViewModel.md)
- [FormApiSectionsV1SectionUpdatedResponse](docs/Model/FormApiSectionsV1SectionUpdatedResponse.md)
- [FormApiSectionsV1UpdateSectionRequest](docs/Model/FormApiSectionsV1UpdateSectionRequest.md)
- [FormApiSubmissionsV1CreateSubmissionRequest](docs/Model/FormApiSubmissionsV1CreateSubmissionRequest.md)
- [FormApiSubmissionsV1ExportStatus](docs/Model/FormApiSubmissionsV1ExportStatus.md)
- [FormApiSubmissionsV1ExportType](docs/Model/FormApiSubmissionsV1ExportType.md)
- [FormApiSubmissionsV1SubmissionCreatedResponse](docs/Model/FormApiSubmissionsV1SubmissionCreatedResponse.md)
- [FormApiSubmissionsV1SubmissionDeletedResponse](docs/Model/FormApiSubmissionsV1SubmissionDeletedResponse.md)
- [FormApiSubmissionsV1SubmissionResponse](docs/Model/FormApiSubmissionsV1SubmissionResponse.md)
- [FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel](docs/Model/FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel.md)
- [FormApiSubmissionsV1SubmissionUpdatedResponse](docs/Model/FormApiSubmissionsV1SubmissionUpdatedResponse.md)
- [FormApiSubmissionsV1SubmissionsExportedResponse](docs/Model/FormApiSubmissionsV1SubmissionsExportedResponse.md)
- [FormApiSubmissionsV1UpdateSubmissionRequest](docs/Model/FormApiSubmissionsV1UpdateSubmissionRequest.md)
- [GoogleProtobufWellKnownTypesListValue](docs/Model/GoogleProtobufWellKnownTypesListValue.md)
- [GoogleProtobufWellKnownTypesNullValue](docs/Model/GoogleProtobufWellKnownTypesNullValue.md)
- [GoogleProtobufWellKnownTypesStruct](docs/Model/GoogleProtobufWellKnownTypesStruct.md)
- [GoogleProtobufWellKnownTypesValue](docs/Model/GoogleProtobufWellKnownTypesValue.md)
- [GoogleProtobufWellKnownTypesValueKindOneofCase](docs/Model/GoogleProtobufWellKnownTypesValueKindOneofCase.md)
- [IMSAdminApiV1ClientsAccessTokenType](docs/Model/IMSAdminApiV1ClientsAccessTokenType.md)
- [IMSAdminApiV1ClientsAddClientSecretRequest](docs/Model/IMSAdminApiV1ClientsAddClientSecretRequest.md)
- [IMSAdminApiV1ClientsClaim](docs/Model/IMSAdminApiV1ClientsClaim.md)
- [IMSAdminApiV1ClientsClientCreatedResponse](docs/Model/IMSAdminApiV1ClientsClientCreatedResponse.md)
- [IMSAdminApiV1ClientsClientDeletedResponse](docs/Model/IMSAdminApiV1ClientsClientDeletedResponse.md)
- [IMSAdminApiV1ClientsClientListResponse](docs/Model/IMSAdminApiV1ClientsClientListResponse.md)
- [IMSAdminApiV1ClientsClientProfileResponse](docs/Model/IMSAdminApiV1ClientsClientProfileResponse.md)
- [IMSAdminApiV1ClientsClientSecretAddedResponse](docs/Model/IMSAdminApiV1ClientsClientSecretAddedResponse.md)
- [IMSAdminApiV1ClientsClientSecretRegeneratedResponse](docs/Model/IMSAdminApiV1ClientsClientSecretRegeneratedResponse.md)
- [IMSAdminApiV1ClientsClientUpdatedResponse](docs/Model/IMSAdminApiV1ClientsClientUpdatedResponse.md)
- [IMSAdminApiV1ClientsPaginatedItemsResponse](docs/Model/IMSAdminApiV1ClientsPaginatedItemsResponse.md)
- [IMSAdminApiV1ClientsRegenerateClientSecretRequest](docs/Model/IMSAdminApiV1ClientsRegenerateClientSecretRequest.md)
- [IMSAdminApiV1ClientsSecret](docs/Model/IMSAdminApiV1ClientsSecret.md)
- [IMSAdminApiV1ClientsTokenExpiration](docs/Model/IMSAdminApiV1ClientsTokenExpiration.md)
- [IMSAdminApiV1ClientsTokenUsage](docs/Model/IMSAdminApiV1ClientsTokenUsage.md)
- [IMSAdminApiV1ClientsUpdateClientRequest](docs/Model/IMSAdminApiV1ClientsUpdateClientRequest.md)
- [IMSAdminApiV1ConnectionsConnectionDetails](docs/Model/IMSAdminApiV1ConnectionsConnectionDetails.md)
- [IMSAdminApiV1ConnectionsConnectionDetailsMetadata](docs/Model/IMSAdminApiV1ConnectionsConnectionDetailsMetadata.md)
- [IMSAdminApiV1ConnectionsConnectionListResponse](docs/Model/IMSAdminApiV1ConnectionsConnectionListResponse.md)
- [IMSAdminApiV1ConnectionsConnectionProfileResponse](docs/Model/IMSAdminApiV1ConnectionsConnectionProfileResponse.md)
- [IMSAdminApiV1ConnectionsConnectionTestedResponse](docs/Model/IMSAdminApiV1ConnectionsConnectionTestedResponse.md)
- [IMSAdminApiV1ConnectionsPagedConnectionsResponse](docs/Model/IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)
- [IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest](docs/Model/IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest.md)
- [IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest](docs/Model/IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest.md)
- [IMSAdminApiV1ConnectionsTestConnectionDetailsRequest](docs/Model/IMSAdminApiV1ConnectionsTestConnectionDetailsRequest.md)
- [IMSAdminApiV1DbBackupCodesDbBackupCode](docs/Model/IMSAdminApiV1DbBackupCodesDbBackupCode.md)
- [IMSAdminApiV1InstancesCreateInstanceRequest](docs/Model/IMSAdminApiV1InstancesCreateInstanceRequest.md)
- [IMSAdminApiV1InstancesExportState](docs/Model/IMSAdminApiV1InstancesExportState.md)
- [IMSAdminApiV1InstancesGetInstanceCsvExportResponse](docs/Model/IMSAdminApiV1InstancesGetInstanceCsvExportResponse.md)
- [IMSAdminApiV1InstancesInstanceCsvExportedResponse](docs/Model/IMSAdminApiV1InstancesInstanceCsvExportedResponse.md)
- [IMSAdminApiV1InstancesInstanceEndpointsResponse](docs/Model/IMSAdminApiV1InstancesInstanceEndpointsResponse.md)
- [IMSAdminApiV1InstancesInstanceListResponse](docs/Model/IMSAdminApiV1InstancesInstanceListResponse.md)
- [IMSAdminApiV1InstancesInstanceProfileResponse](docs/Model/IMSAdminApiV1InstancesInstanceProfileResponse.md)
- [IMSAdminApiV1InstancesInstanceResetResponse](docs/Model/IMSAdminApiV1InstancesInstanceResetResponse.md)
- [IMSAdminApiV1InstancesInstanceTruncatedResponse](docs/Model/IMSAdminApiV1InstancesInstanceTruncatedResponse.md)
- [IMSAdminApiV1InstancesPagedInstancesResponse](docs/Model/IMSAdminApiV1InstancesPagedInstancesResponse.md)
- [IMSAdminApiV1InstancesUpdateInstanceRequest](docs/Model/IMSAdminApiV1InstancesUpdateInstanceRequest.md)
- [IMSAdminApiV1TiersTier](docs/Model/IMSAdminApiV1TiersTier.md)
- [IdentityApiApiClientV1AccessTokenType](docs/Model/IdentityApiApiClientV1AccessTokenType.md)
- [IdentityApiApiClientV1ApiClaim](docs/Model/IdentityApiApiClientV1ApiClaim.md)
- [IdentityApiApiClientV1ApiClientCreatedResponse](docs/Model/IdentityApiApiClientV1ApiClientCreatedResponse.md)
- [IdentityApiApiClientV1ApiClientListResponse](docs/Model/IdentityApiApiClientV1ApiClientListResponse.md)
- [IdentityApiApiClientV1ApiClientPaginatedItemsResponse](docs/Model/IdentityApiApiClientV1ApiClientPaginatedItemsResponse.md)
- [IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel](docs/Model/IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel.md)
- [IdentityApiApiClientV1ApiClientProfileResponse](docs/Model/IdentityApiApiClientV1ApiClientProfileResponse.md)
- [IdentityApiApiClientV1ApiClientSecretRegeneratedResponse](docs/Model/IdentityApiApiClientV1ApiClientSecretRegeneratedResponse.md)
- [IdentityApiApiClientV1ApiClientUpdatedResponse](docs/Model/IdentityApiApiClientV1ApiClientUpdatedResponse.md)
- [IdentityApiApiClientV1Claim](docs/Model/IdentityApiApiClientV1Claim.md)
- [IdentityApiApiClientV1CreateApiClientRequest](docs/Model/IdentityApiApiClientV1CreateApiClientRequest.md)
- [IdentityApiApiClientV1RegenerateApiClientSecretRequest](docs/Model/IdentityApiApiClientV1RegenerateApiClientSecretRequest.md)
- [IdentityApiApiClientV1TokenExpiration](docs/Model/IdentityApiApiClientV1TokenExpiration.md)
- [IdentityApiApiClientV1TokenUsage](docs/Model/IdentityApiApiClientV1TokenUsage.md)
- [IdentityApiApiClientV1UpdateApiClientRequest](docs/Model/IdentityApiApiClientV1UpdateApiClientRequest.md)
- [IdentityApiClientSettingsTypeV1ClientSettingsTypeResponse](docs/Model/IdentityApiClientSettingsTypeV1ClientSettingsTypeResponse.md)
- [IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse](docs/Model/IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse.md)
- [IdentityApiInstructionalInsightsV1CallbackNotificationMessage](docs/Model/IdentityApiInstructionalInsightsV1CallbackNotificationMessage.md)
- [IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest](docs/Model/IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionLogMessage](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionLogMessage.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMessage](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMessage.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMetricMessage](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMetricMessage.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobInputMessage](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobInputMessage.md)
- [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse](docs/Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse.md)
- [IdentityApiInstructionalInsightsV1JobExecutionMessage](docs/Model/IdentityApiInstructionalInsightsV1JobExecutionMessage.md)
- [IdentityApiInstructionalInsightsV1RetryPolicyMessage](docs/Model/IdentityApiInstructionalInsightsV1RetryPolicyMessage.md)
- [IdentityApiInstructionalInsightsV1ScheduleMessage](docs/Model/IdentityApiInstructionalInsightsV1ScheduleMessage.md)
- [IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse](docs/Model/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse.md)
- [IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse](docs/Model/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse.md)
- [IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest](docs/Model/IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest.md)
- [IdentityApiInvitationV1AssignLicenseRequest](docs/Model/IdentityApiInvitationV1AssignLicenseRequest.md)
- [IdentityApiInvitationV1InvitationListResponse](docs/Model/IdentityApiInvitationV1InvitationListResponse.md)
- [IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel](docs/Model/IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel.md)
- [IdentityApiInvitationV1InvitationResponse](docs/Model/IdentityApiInvitationV1InvitationResponse.md)
- [IdentityApiInvitationV1InvitationSentResponse](docs/Model/IdentityApiInvitationV1InvitationSentResponse.md)
- [IdentityApiInvitationV1InvitationStatus](docs/Model/IdentityApiInvitationV1InvitationStatus.md)
- [IdentityApiStaffClassificationV1CreateStaffClassificationRequest](docs/Model/IdentityApiStaffClassificationV1CreateStaffClassificationRequest.md)
- [IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse](docs/Model/IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse.md)
- [IdentityApiStaffClassificationV1GetStaffClassificationsResponse](docs/Model/IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)
- [IdentityApiStaffClassificationV1StaffClassificationCreatedResponse](docs/Model/IdentityApiStaffClassificationV1StaffClassificationCreatedResponse.md)
- [IdentityApiStaffClassificationV1StaffClassificationDeletedResponse](docs/Model/IdentityApiStaffClassificationV1StaffClassificationDeletedResponse.md)
- [IdentityApiStaffClassificationV1StaffClassificationLicense](docs/Model/IdentityApiStaffClassificationV1StaffClassificationLicense.md)
- [IdentityApiStaffClassificationV1StaffClassificationLicenseRequest](docs/Model/IdentityApiStaffClassificationV1StaffClassificationLicenseRequest.md)
- [IdentityApiStaffClassificationV1StaffClassificationResponse](docs/Model/IdentityApiStaffClassificationV1StaffClassificationResponse.md)
- [IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse](docs/Model/IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse.md)
- [IdentityApiStaffClassificationV1UpdateStaffClassificationRequest](docs/Model/IdentityApiStaffClassificationV1UpdateStaffClassificationRequest.md)
- [IdentityApiUserV1ActivateUserRequest](docs/Model/IdentityApiUserV1ActivateUserRequest.md)
- [IdentityApiUserV1AddSectionBulkRequest](docs/Model/IdentityApiUserV1AddSectionBulkRequest.md)
- [IdentityApiUserV1AddSectionBulkRequestTypesSectionDto](docs/Model/IdentityApiUserV1AddSectionBulkRequestTypesSectionDto.md)
- [IdentityApiUserV1AddSectionRequest](docs/Model/IdentityApiUserV1AddSectionRequest.md)
- [IdentityApiUserV1DeactivateUserRequest](docs/Model/IdentityApiUserV1DeactivateUserRequest.md)
- [IdentityApiUserV1EducationOrganization](docs/Model/IdentityApiUserV1EducationOrganization.md)
- [IdentityApiUserV1EducationOrganizationAddedResponse](docs/Model/IdentityApiUserV1EducationOrganizationAddedResponse.md)
- [IdentityApiUserV1EducationOrganizationPaginatedItemsResponse](docs/Model/IdentityApiUserV1EducationOrganizationPaginatedItemsResponse.md)
- [IdentityApiUserV1EducationOrganizationRemovedResponse](docs/Model/IdentityApiUserV1EducationOrganizationRemovedResponse.md)
- [IdentityApiUserV1EducationOrganizationUpdatedResponse](docs/Model/IdentityApiUserV1EducationOrganizationUpdatedResponse.md)
- [IdentityApiUserV1GetSEOAAsResponse](docs/Model/IdentityApiUserV1GetSEOAAsResponse.md)
- [IdentityApiUserV1GetSectionsResponse](docs/Model/IdentityApiUserV1GetSectionsResponse.md)
- [IdentityApiUserV1GetUserPreferencesResponse](docs/Model/IdentityApiUserV1GetUserPreferencesResponse.md)
- [IdentityApiUserV1LicenseAssignedBulkResponse](docs/Model/IdentityApiUserV1LicenseAssignedBulkResponse.md)
- [IdentityApiUserV1LicenseAssignedResponse](docs/Model/IdentityApiUserV1LicenseAssignedResponse.md)
- [IdentityApiUserV1LicenseRevokedBulkResponse](docs/Model/IdentityApiUserV1LicenseRevokedBulkResponse.md)
- [IdentityApiUserV1LicenseRevokedResponse](docs/Model/IdentityApiUserV1LicenseRevokedResponse.md)
- [IdentityApiUserV1LocalUserCreatedResponse](docs/Model/IdentityApiUserV1LocalUserCreatedResponse.md)
- [IdentityApiUserV1PasswordResettedResponse](docs/Model/IdentityApiUserV1PasswordResettedResponse.md)
- [IdentityApiUserV1Preference](docs/Model/IdentityApiUserV1Preference.md)
- [IdentityApiUserV1ReleaseUserLockoutResponse](docs/Model/IdentityApiUserV1ReleaseUserLockoutResponse.md)
- [IdentityApiUserV1RemoveSectionBulkRequest](docs/Model/IdentityApiUserV1RemoveSectionBulkRequest.md)
- [IdentityApiUserV1ResetPasswordRequest](docs/Model/IdentityApiUserV1ResetPasswordRequest.md)
- [IdentityApiUserV1RevokeLicenseRequest](docs/Model/IdentityApiUserV1RevokeLicenseRequest.md)
- [IdentityApiUserV1RevokeStrategy](docs/Model/IdentityApiUserV1RevokeStrategy.md)
- [IdentityApiUserV1SEOAAAddedResponse](docs/Model/IdentityApiUserV1SEOAAAddedResponse.md)
- [IdentityApiUserV1SEOAAResponse](docs/Model/IdentityApiUserV1SEOAAResponse.md)
- [IdentityApiUserV1SEOAAUpdatedResponse](docs/Model/IdentityApiUserV1SEOAAUpdatedResponse.md)
- [IdentityApiUserV1SectionAddedBulkResponse](docs/Model/IdentityApiUserV1SectionAddedBulkResponse.md)
- [IdentityApiUserV1SectionAddedResponse](docs/Model/IdentityApiUserV1SectionAddedResponse.md)
- [IdentityApiUserV1SectionRemovedBulkResponse](docs/Model/IdentityApiUserV1SectionRemovedBulkResponse.md)
- [IdentityApiUserV1SectionRemovedResponse](docs/Model/IdentityApiUserV1SectionRemovedResponse.md)
- [IdentityApiUserV1SectionResponse](docs/Model/IdentityApiUserV1SectionResponse.md)
- [IdentityApiUserV1SectionResponseGetPaginatedItemsResponse](docs/Model/IdentityApiUserV1SectionResponseGetPaginatedItemsResponse.md)
- [IdentityApiUserV1SectionUpdatedBulkResponse](docs/Model/IdentityApiUserV1SectionUpdatedBulkResponse.md)
- [IdentityApiUserV1SectionUpdatedResponse](docs/Model/IdentityApiUserV1SectionUpdatedResponse.md)
- [IdentityApiUserV1SetUserExtensionRequest](docs/Model/IdentityApiUserV1SetUserExtensionRequest.md)
- [IdentityApiUserV1TenantStatus](docs/Model/IdentityApiUserV1TenantStatus.md)
- [IdentityApiUserV1TenantType](docs/Model/IdentityApiUserV1TenantType.md)
- [IdentityApiUserV1UpdateSectionBulkRequest](docs/Model/IdentityApiUserV1UpdateSectionBulkRequest.md)
- [IdentityApiUserV1UpdateSectionBulkRequestTypesSectionDto](docs/Model/IdentityApiUserV1UpdateSectionBulkRequestTypesSectionDto.md)
- [IdentityApiUserV1UpdateSectionRequest](docs/Model/IdentityApiUserV1UpdateSectionRequest.md)
- [IdentityApiUserV1UserActivatedResponse](docs/Model/IdentityApiUserV1UserActivatedResponse.md)
- [IdentityApiUserV1UserDeactivatedResponse](docs/Model/IdentityApiUserV1UserDeactivatedResponse.md)
- [IdentityApiUserV1UserExtension](docs/Model/IdentityApiUserV1UserExtension.md)
- [IdentityApiUserV1UserExtensionRemovedResponse](docs/Model/IdentityApiUserV1UserExtensionRemovedResponse.md)
- [IdentityApiUserV1UserExtensionSetResponse](docs/Model/IdentityApiUserV1UserExtensionSetResponse.md)
- [IdentityApiUserV1UserPreferenceUpdatedResponse](docs/Model/IdentityApiUserV1UserPreferenceUpdatedResponse.md)
- [IdentityApiUserV1UserTenantProfile](docs/Model/IdentityApiUserV1UserTenantProfile.md)
- [IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel](docs/Model/IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel.md)
- [IdentityApiUserV1UserTenantProfileTypesUserTenantEducationOrganizationProfile](docs/Model/IdentityApiUserV1UserTenantProfileTypesUserTenantEducationOrganizationProfile.md)
- [IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfile](docs/Model/IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfile.md)
- [IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfileTypesUserTenantLicenseRoleProfile](docs/Model/IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfileTypesUserTenantLicenseRoleProfile.md)
- [IdentityApiUserV1UserTenantStatusProfile](docs/Model/IdentityApiUserV1UserTenantStatusProfile.md)
- [IdentityApiUserV1UserUpdatedResponse](docs/Model/IdentityApiUserV1UserUpdatedResponse.md)
- [IdentityApiUserV2TenantMeProfile](docs/Model/IdentityApiUserV2TenantMeProfile.md)
- [IdentityApiUserV2UserExtension](docs/Model/IdentityApiUserV2UserExtension.md)
- [IdentityApiUserV2UserLicenseProfileResponse](docs/Model/IdentityApiUserV2UserLicenseProfileResponse.md)
- [IdentityApiUserV2UserLicenseRole](docs/Model/IdentityApiUserV2UserLicenseRole.md)
- [IdentityApiUserV2UserLicensesResponse](docs/Model/IdentityApiUserV2UserLicensesResponse.md)
- [IdentityApiUserV2UserLogin](docs/Model/IdentityApiUserV2UserLogin.md)
- [IdentityApiUserV2UserMeProfile](docs/Model/IdentityApiUserV2UserMeProfile.md)
- [IdentityApiUserV2UserMeTenantsResponse](docs/Model/IdentityApiUserV2UserMeTenantsResponse.md)
- [IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel](docs/Model/IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)
- [IdentityApiUserV2UserProfileResponse](docs/Model/IdentityApiUserV2UserProfileResponse.md)
- [IdentityApiUserV2UserTenantProfileResponse](docs/Model/IdentityApiUserV2UserTenantProfileResponse.md)
- [IdentityApiUserV2UsersSearchResponse](docs/Model/IdentityApiUserV2UsersSearchResponse.md)
- [MicrosoftAspNetCoreMvcNoContentResult](docs/Model/MicrosoftAspNetCoreMvcNoContentResult.md)
- [MicrosoftAspNetCoreMvcProblemDetails](docs/Model/MicrosoftAspNetCoreMvcProblemDetails.md)
- [MicrosoftAspNetCoreMvcValidationProblemDetails](docs/Model/MicrosoftAspNetCoreMvcValidationProblemDetails.md)
- [RegistrationApiRegistrationV2ApprovalStatus](docs/Model/RegistrationApiRegistrationV2ApprovalStatus.md)
- [RegistrationApiRegistrationV2SubmitTenantRegistrationRequest](docs/Model/RegistrationApiRegistrationV2SubmitTenantRegistrationRequest.md)
- [RegistrationApiRegistrationV2TenantType](docs/Model/RegistrationApiRegistrationV2TenantType.md)
- [TenantApiIntegrationsV1CreateIntegrationProductRequest](docs/Model/TenantApiIntegrationsV1CreateIntegrationProductRequest.md)
- [TenantApiIntegrationsV1CreateIntegrationProductResponse](docs/Model/TenantApiIntegrationsV1CreateIntegrationProductResponse.md)
- [TenantApiIntegrationsV1CreateIntegrationRequest](docs/Model/TenantApiIntegrationsV1CreateIntegrationRequest.md)
- [TenantApiIntegrationsV1CreateIntegrationResponse](docs/Model/TenantApiIntegrationsV1CreateIntegrationResponse.md)
- [TenantApiIntegrationsV1CreateIntegrationTypeRequest](docs/Model/TenantApiIntegrationsV1CreateIntegrationTypeRequest.md)
- [TenantApiIntegrationsV1CreateIntegrationTypeResponse](docs/Model/TenantApiIntegrationsV1CreateIntegrationTypeResponse.md)
- [TenantApiIntegrationsV1CreateIntegrationVendorRequest](docs/Model/TenantApiIntegrationsV1CreateIntegrationVendorRequest.md)
- [TenantApiIntegrationsV1CreateIntegrationVendorResponse](docs/Model/TenantApiIntegrationsV1CreateIntegrationVendorResponse.md)
- [TenantApiIntegrationsV1DeleteIntegrationProductResponse](docs/Model/TenantApiIntegrationsV1DeleteIntegrationProductResponse.md)
- [TenantApiIntegrationsV1DeleteIntegrationResponse](docs/Model/TenantApiIntegrationsV1DeleteIntegrationResponse.md)
- [TenantApiIntegrationsV1DeleteIntegrationTypeResponse](docs/Model/TenantApiIntegrationsV1DeleteIntegrationTypeResponse.md)
- [TenantApiIntegrationsV1DeleteIntegrationVendorResponse](docs/Model/TenantApiIntegrationsV1DeleteIntegrationVendorResponse.md)
- [TenantApiIntegrationsV1GetIntegrationProductResponse](docs/Model/TenantApiIntegrationsV1GetIntegrationProductResponse.md)
- [TenantApiIntegrationsV1GetIntegrationResponse](docs/Model/TenantApiIntegrationsV1GetIntegrationResponse.md)
- [TenantApiIntegrationsV1GetIntegrationTypeResponse](docs/Model/TenantApiIntegrationsV1GetIntegrationTypeResponse.md)
- [TenantApiIntegrationsV1GetIntegrationVendorResponse](docs/Model/TenantApiIntegrationsV1GetIntegrationVendorResponse.md)
- [TenantApiIntegrationsV1Integration](docs/Model/TenantApiIntegrationsV1Integration.md)
- [TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel](docs/Model/TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel.md)
- [TenantApiIntegrationsV1IntegrationProduct](docs/Model/TenantApiIntegrationsV1IntegrationProduct.md)
- [TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel](docs/Model/TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel.md)
- [TenantApiIntegrationsV1IntegrationType](docs/Model/TenantApiIntegrationsV1IntegrationType.md)
- [TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel](docs/Model/TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel.md)
- [TenantApiIntegrationsV1IntegrationVendor](docs/Model/TenantApiIntegrationsV1IntegrationVendor.md)
- [TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel](docs/Model/TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel.md)
- [TenantApiIntegrationsV1UpdateIntegrationProductRequest](docs/Model/TenantApiIntegrationsV1UpdateIntegrationProductRequest.md)
- [TenantApiIntegrationsV1UpdateIntegrationRequest](docs/Model/TenantApiIntegrationsV1UpdateIntegrationRequest.md)
- [TenantApiIntegrationsV1UpdateIntegrationTypeRequest](docs/Model/TenantApiIntegrationsV1UpdateIntegrationTypeRequest.md)
- [TenantApiIntegrationsV1UpdateIntegrationVendorRequest](docs/Model/TenantApiIntegrationsV1UpdateIntegrationVendorRequest.md)
- [TenantApiPartnershipV1PaginatedItemsResponse](docs/Model/TenantApiPartnershipV1PaginatedItemsResponse.md)
- [TenantApiPartnershipV1ParternshipTenantResponse](docs/Model/TenantApiPartnershipV1ParternshipTenantResponse.md)
- [TenantApiPartnershipV1PartnershipByIdResponse](docs/Model/TenantApiPartnershipV1PartnershipByIdResponse.md)
- [TenantApiPartnershipV1PartnershipResponse](docs/Model/TenantApiPartnershipV1PartnershipResponse.md)
- [TenantApiPartnershipV1PartnershipSyncDTO](docs/Model/TenantApiPartnershipV1PartnershipSyncDTO.md)
- [TenantApiPartnershipV1PartnershipSyncDirection](docs/Model/TenantApiPartnershipV1PartnershipSyncDirection.md)
- [TenantApiPartnershipV1PartnershipSyncType](docs/Model/TenantApiPartnershipV1PartnershipSyncType.md)
- [TenantApiPartnershipV1TenantType](docs/Model/TenantApiPartnershipV1TenantType.md)
- [TenantApiSectionsV1AcademicSubjectListResponse](docs/Model/TenantApiSectionsV1AcademicSubjectListResponse.md)
- [TenantApiSectionsV1CourseListResponse](docs/Model/TenantApiSectionsV1CourseListResponse.md)
- [TenantApiSectionsV1GradeLevelListResponse](docs/Model/TenantApiSectionsV1GradeLevelListResponse.md)
- [TenantApiSectionsV1PaginatedAcademicSubjectsResponse](docs/Model/TenantApiSectionsV1PaginatedAcademicSubjectsResponse.md)
- [TenantApiSectionsV1PaginatedCoursesResponse](docs/Model/TenantApiSectionsV1PaginatedCoursesResponse.md)
- [TenantApiSectionsV1PaginatedGradeLevelsResponse](docs/Model/TenantApiSectionsV1PaginatedGradeLevelsResponse.md)
- [TenantApiSectionsV1PaginatedItemsResponse](docs/Model/TenantApiSectionsV1PaginatedItemsResponse.md)
- [TenantApiSectionsV1PaginatedSchoolsResponse](docs/Model/TenantApiSectionsV1PaginatedSchoolsResponse.md)
- [TenantApiSectionsV1PaginatedSessionsResponse](docs/Model/TenantApiSectionsV1PaginatedSessionsResponse.md)
- [TenantApiSectionsV1PaginatedTermsResponse](docs/Model/TenantApiSectionsV1PaginatedTermsResponse.md)
- [TenantApiSectionsV1SchoolListResponse](docs/Model/TenantApiSectionsV1SchoolListResponse.md)
- [TenantApiSectionsV1SectionListResponse](docs/Model/TenantApiSectionsV1SectionListResponse.md)
- [TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse](docs/Model/TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse.md)
- [TenantApiSectionsV1SectionProfileResponse](docs/Model/TenantApiSectionsV1SectionProfileResponse.md)
- [TenantApiSectionsV1SectionSource](docs/Model/TenantApiSectionsV1SectionSource.md)
- [TenantApiSectionsV1SessionListResponse](docs/Model/TenantApiSectionsV1SessionListResponse.md)
- [TenantApiSectionsV1TermListResponse](docs/Model/TenantApiSectionsV1TermListResponse.md)
- [TenantApiTenantV1CreateDomainRequest](docs/Model/TenantApiTenantV1CreateDomainRequest.md)
- [TenantApiTenantV1CreateOrganizationRequest](docs/Model/TenantApiTenantV1CreateOrganizationRequest.md)
- [TenantApiTenantV1CreateSubscriptionRequest](docs/Model/TenantApiTenantV1CreateSubscriptionRequest.md)
- [TenantApiTenantV1DeploymentType](docs/Model/TenantApiTenantV1DeploymentType.md)
- [TenantApiTenantV1DomainCreatedResponse](docs/Model/TenantApiTenantV1DomainCreatedResponse.md)
- [TenantApiTenantV1DomainProfileResponse](docs/Model/TenantApiTenantV1DomainProfileResponse.md)
- [TenantApiTenantV1DomainStatus](docs/Model/TenantApiTenantV1DomainStatus.md)
- [TenantApiTenantV1DomainUpdatedResponse](docs/Model/TenantApiTenantV1DomainUpdatedResponse.md)
- [TenantApiTenantV1DomainVerifiedResponse](docs/Model/TenantApiTenantV1DomainVerifiedResponse.md)
- [TenantApiTenantV1GetAppSettingsResponse](docs/Model/TenantApiTenantV1GetAppSettingsResponse.md)
- [TenantApiTenantV1GetOrganizationsPaginatedResponse](docs/Model/TenantApiTenantV1GetOrganizationsPaginatedResponse.md)
- [TenantApiTenantV1IdentityProviderId](docs/Model/TenantApiTenantV1IdentityProviderId.md)
- [TenantApiTenantV1IdentityProviderStatus](docs/Model/TenantApiTenantV1IdentityProviderStatus.md)
- [TenantApiTenantV1LicenseType](docs/Model/TenantApiTenantV1LicenseType.md)
- [TenantApiTenantV1Onboarding](docs/Model/TenantApiTenantV1Onboarding.md)
- [TenantApiTenantV1OnboardingStep](docs/Model/TenantApiTenantV1OnboardingStep.md)
- [TenantApiTenantV1OnboardingStepsReponse](docs/Model/TenantApiTenantV1OnboardingStepsReponse.md)
- [TenantApiTenantV1Organization](docs/Model/TenantApiTenantV1Organization.md)
- [TenantApiTenantV1OrganizationCreatedResponse](docs/Model/TenantApiTenantV1OrganizationCreatedResponse.md)
- [TenantApiTenantV1OrganizationDeletedResponse](docs/Model/TenantApiTenantV1OrganizationDeletedResponse.md)
- [TenantApiTenantV1OrganizationGetPaginatedItemsResponse](docs/Model/TenantApiTenantV1OrganizationGetPaginatedItemsResponse.md)
- [TenantApiTenantV1OrganizationUpdatedResponse](docs/Model/TenantApiTenantV1OrganizationUpdatedResponse.md)
- [TenantApiTenantV1SetAppSettingsRequest](docs/Model/TenantApiTenantV1SetAppSettingsRequest.md)
- [TenantApiTenantV1SetAppSettingsResponse](docs/Model/TenantApiTenantV1SetAppSettingsResponse.md)
- [TenantApiTenantV1SubscriptionCreatedResponse](docs/Model/TenantApiTenantV1SubscriptionCreatedResponse.md)
- [TenantApiTenantV1SubscriptionProfileResponse](docs/Model/TenantApiTenantV1SubscriptionProfileResponse.md)
- [TenantApiTenantV1SubscriptionStatus](docs/Model/TenantApiTenantV1SubscriptionStatus.md)
- [TenantApiTenantV1SubscriptionUpdatedResponse](docs/Model/TenantApiTenantV1SubscriptionUpdatedResponse.md)
- [TenantApiTenantV1TenantAdditionalSetting](docs/Model/TenantApiTenantV1TenantAdditionalSetting.md)
- [TenantApiTenantV1TenantAppSettings](docs/Model/TenantApiTenantV1TenantAppSettings.md)
- [TenantApiTenantV1TenantBrandingBackground](docs/Model/TenantApiTenantV1TenantBrandingBackground.md)
- [TenantApiTenantV1TenantBrandingLogo](docs/Model/TenantApiTenantV1TenantBrandingLogo.md)
- [TenantApiTenantV1TenantBrandingResponse](docs/Model/TenantApiTenantV1TenantBrandingResponse.md)
- [TenantApiTenantV1TenantIdentityProviders](docs/Model/TenantApiTenantV1TenantIdentityProviders.md)
- [TenantApiTenantV1TenantProfileResponse](docs/Model/TenantApiTenantV1TenantProfileResponse.md)
- [TenantApiTenantV1TenantSetting](docs/Model/TenantApiTenantV1TenantSetting.md)
- [TenantApiTenantV1TenantSettingTypesListResponse](docs/Model/TenantApiTenantV1TenantSettingTypesListResponse.md)
- [TenantApiTenantV1TenantSettingTypesListResponsePaginatedItemsViewModel](docs/Model/TenantApiTenantV1TenantSettingTypesListResponsePaginatedItemsViewModel.md)
- [TenantApiTenantV1TenantSettingsTypeAttribute](docs/Model/TenantApiTenantV1TenantSettingsTypeAttribute.md)
- [TenantApiTenantV1TenantStatus](docs/Model/TenantApiTenantV1TenantStatus.md)
- [TenantApiTenantV1TenantType](docs/Model/TenantApiTenantV1TenantType.md)
- [TenantApiTenantV1TenantUpdatedResponse](docs/Model/TenantApiTenantV1TenantUpdatedResponse.md)
- [TenantApiTenantV1UpdateDomainRequest](docs/Model/TenantApiTenantV1UpdateDomainRequest.md)
- [TenantApiTenantV1UpdateOrganizationRequest](docs/Model/TenantApiTenantV1UpdateOrganizationRequest.md)
- [TenantApiTenantV1UpdateSubscriptionRequest](docs/Model/TenantApiTenantV1UpdateSubscriptionRequest.md)
- [TenantApiTenantV1VerifyDomainRequest](docs/Model/TenantApiTenantV1VerifyDomainRequest.md)
- [TenantApiWebhookV1CreateWebhookRequest](docs/Model/TenantApiWebhookV1CreateWebhookRequest.md)
- [TenantApiWebhookV1PaginatedItemsResponse](docs/Model/TenantApiWebhookV1PaginatedItemsResponse.md)
- [TenantApiWebhookV1PaginatedWebhookEventItemsResponse](docs/Model/TenantApiWebhookV1PaginatedWebhookEventItemsResponse.md)
- [TenantApiWebhookV1ReRunRequestedResponse](docs/Model/TenantApiWebhookV1ReRunRequestedResponse.md)
- [TenantApiWebhookV1RequestReRunRequest](docs/Model/TenantApiWebhookV1RequestReRunRequest.md)
- [TenantApiWebhookV1UpdateWebhookRequest](docs/Model/TenantApiWebhookV1UpdateWebhookRequest.md)
- [TenantApiWebhookV1WebhookEventResponse](docs/Model/TenantApiWebhookV1WebhookEventResponse.md)
- [TenantApiWebhookV1WebhookIdResponse](docs/Model/TenantApiWebhookV1WebhookIdResponse.md)
- [TenantApiWebhookV1WebhookReRunStrategy](docs/Model/TenantApiWebhookV1WebhookReRunStrategy.md)
- [TenantApiWebhookV1WebhookResponse](docs/Model/TenantApiWebhookV1WebhookResponse.md)
- [TenantApiWebhookV1WebhookSchema](docs/Model/TenantApiWebhookV1WebhookSchema.md)
- [TenantApiWebhookV1WebhookSubscriberResponse](docs/Model/TenantApiWebhookV1WebhookSubscriberResponse.md)
- [ValidationsApiContainersV1AddDataStewardBulkRequest](docs/Model/ValidationsApiContainersV1AddDataStewardBulkRequest.md)
- [ValidationsApiContainersV1AddDataStewardBulkRequestTypesCollection](docs/Model/ValidationsApiContainersV1AddDataStewardBulkRequestTypesCollection.md)
- [ValidationsApiContainersV1AddDataStewardRequest](docs/Model/ValidationsApiContainersV1AddDataStewardRequest.md)
- [ValidationsApiContainersV1CategoriesWithDataUsersResponse](docs/Model/ValidationsApiContainersV1CategoriesWithDataUsersResponse.md)
- [ValidationsApiContainersV1CertificationReminderRequestedResponse](docs/Model/ValidationsApiContainersV1CertificationReminderRequestedResponse.md)
- [ValidationsApiContainersV1CertificationStatusSetResponse](docs/Model/ValidationsApiContainersV1CertificationStatusSetResponse.md)
- [ValidationsApiContainersV1CollectionUploadedResponse](docs/Model/ValidationsApiContainersV1CollectionUploadedResponse.md)
- [ValidationsApiContainersV1CollectionUploadedResponseTypesUploadResult](docs/Model/ValidationsApiContainersV1CollectionUploadedResponseTypesUploadResult.md)
- [ValidationsApiContainersV1CollectionUser](docs/Model/ValidationsApiContainersV1CollectionUser.md)
- [ValidationsApiContainersV1ContainerDto](docs/Model/ValidationsApiContainersV1ContainerDto.md)
- [ValidationsApiContainersV1ContainerDtoTypesTagDto](docs/Model/ValidationsApiContainersV1ContainerDtoTypesTagDto.md)
- [ValidationsApiContainersV1CreateCollectionRequest](docs/Model/ValidationsApiContainersV1CreateCollectionRequest.md)
- [ValidationsApiContainersV1CreateContainerRequest](docs/Model/ValidationsApiContainersV1CreateContainerRequest.md)
- [ValidationsApiContainersV1DataOwnerSetBulkResponse](docs/Model/ValidationsApiContainersV1DataOwnerSetBulkResponse.md)
- [ValidationsApiContainersV1DataOwnerSetBulkResponseTypesCollection](docs/Model/ValidationsApiContainersV1DataOwnerSetBulkResponseTypesCollection.md)
- [ValidationsApiContainersV1DataOwnerSetResponse](docs/Model/ValidationsApiContainersV1DataOwnerSetResponse.md)
- [ValidationsApiContainersV1DataStewardAddedBulkResponse](docs/Model/ValidationsApiContainersV1DataStewardAddedBulkResponse.md)
- [ValidationsApiContainersV1DataStewardAddedBulkResponseTypesCollection](docs/Model/ValidationsApiContainersV1DataStewardAddedBulkResponseTypesCollection.md)
- [ValidationsApiContainersV1DataStewardAddedResponse](docs/Model/ValidationsApiContainersV1DataStewardAddedResponse.md)
- [ValidationsApiContainersV1DataUserResponse](docs/Model/ValidationsApiContainersV1DataUserResponse.md)
- [ValidationsApiContainersV1GetJsonResponse](docs/Model/ValidationsApiContainersV1GetJsonResponse.md)
- [ValidationsApiContainersV1PaginatedCategoryTreeResponse](docs/Model/ValidationsApiContainersV1PaginatedCategoryTreeResponse.md)
- [ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesCategoryTree](docs/Model/ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesCategoryTree.md)
- [ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesSubCategoryTree](docs/Model/ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesSubCategoryTree.md)
- [ValidationsApiContainersV1PaginatedContainers](docs/Model/ValidationsApiContainersV1PaginatedContainers.md)
- [ValidationsApiContainersV1SetDataOwnerBulkRequest](docs/Model/ValidationsApiContainersV1SetDataOwnerBulkRequest.md)
- [ValidationsApiContainersV1SetDataOwnerBulkRequestTypesCollection](docs/Model/ValidationsApiContainersV1SetDataOwnerBulkRequestTypesCollection.md)
- [ValidationsApiContainersV1SetDataOwnerRequest](docs/Model/ValidationsApiContainersV1SetDataOwnerRequest.md)
- [ValidationsApiContainersV1UpdateCollectionRequest](docs/Model/ValidationsApiContainersV1UpdateCollectionRequest.md)
- [ValidationsApiContainersV1UpdateContainerRequest](docs/Model/ValidationsApiContainersV1UpdateContainerRequest.md)
- [ValidationsApiContainersV1UploadCollectionRequest](docs/Model/ValidationsApiContainersV1UploadCollectionRequest.md)
- [ValidationsApiContainersV1Url](docs/Model/ValidationsApiContainersV1Url.md)
- [ValidationsApiCoreV1CreatedResponse](docs/Model/ValidationsApiCoreV1CreatedResponse.md)
- [ValidationsApiCoreV1InstanceType](docs/Model/ValidationsApiCoreV1InstanceType.md)
- [ValidationsApiCoreV1Provider](docs/Model/ValidationsApiCoreV1Provider.md)
- [ValidationsApiDbEnvironmentsV1AzureSynapseSqlServerlessConnection](docs/Model/ValidationsApiDbEnvironmentsV1AzureSynapseSqlServerlessConnection.md)
- [ValidationsApiDbEnvironmentsV1CreateRequest](docs/Model/ValidationsApiDbEnvironmentsV1CreateRequest.md)
- [ValidationsApiDbEnvironmentsV1DbEnvironmentDto](docs/Model/ValidationsApiDbEnvironmentsV1DbEnvironmentDto.md)
- [ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments](docs/Model/ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments.md)
- [ValidationsApiDbEnvironmentsV1SqlServerConnection](docs/Model/ValidationsApiDbEnvironmentsV1SqlServerConnection.md)
- [ValidationsApiDbEnvironmentsV1TestConnectionRequest](docs/Model/ValidationsApiDbEnvironmentsV1TestConnectionRequest.md)
- [ValidationsApiDbEnvironmentsV1TestConnectionResponse](docs/Model/ValidationsApiDbEnvironmentsV1TestConnectionResponse.md)
- [ValidationsApiDbEnvironmentsV1UpdateRequest](docs/Model/ValidationsApiDbEnvironmentsV1UpdateRequest.md)
- [ValidationsApiJobsV1ChildJob](docs/Model/ValidationsApiJobsV1ChildJob.md)
- [ValidationsApiJobsV1DataRefreshType](docs/Model/ValidationsApiJobsV1DataRefreshType.md)
- [ValidationsApiJobsV1JobExecutionStatus](docs/Model/ValidationsApiJobsV1JobExecutionStatus.md)
- [ValidationsApiJobsV1JobListResponse](docs/Model/ValidationsApiJobsV1JobListResponse.md)
- [ValidationsApiJobsV1JobMetadata](docs/Model/ValidationsApiJobsV1JobMetadata.md)
- [ValidationsApiJobsV1JobProfileResponse](docs/Model/ValidationsApiJobsV1JobProfileResponse.md)
- [ValidationsApiJobsV1JobStatus](docs/Model/ValidationsApiJobsV1JobStatus.md)
- [ValidationsApiJobsV1Metric](docs/Model/ValidationsApiJobsV1Metric.md)
- [ValidationsApiJobsV1PaginatedItemsResponse](docs/Model/ValidationsApiJobsV1PaginatedItemsResponse.md)
- [ValidationsApiJobsV1Schedule](docs/Model/ValidationsApiJobsV1Schedule.md)
- [ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest](docs/Model/ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest.md)
- [ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest](docs/Model/ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest.md)
- [ValidationsApiReportingPeriodsV1CertificationStatus](docs/Model/ValidationsApiReportingPeriodsV1CertificationStatus.md)
- [ValidationsApiReportingPeriodsV1CertificationStatusCategory](docs/Model/ValidationsApiReportingPeriodsV1CertificationStatusCategory.md)
- [ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse](docs/Model/ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse.md)
- [ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse](docs/Model/ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse.md)
- [ValidationsApiReportingPeriodsV1PaginatedRecords](docs/Model/ValidationsApiReportingPeriodsV1PaginatedRecords.md)
- [ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecords](docs/Model/ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecords.md)
- [ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule](docs/Model/ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule.md)
- [ValidationsApiReportingPeriodsV1PaginatedReportingPeriods](docs/Model/ValidationsApiReportingPeriodsV1PaginatedReportingPeriods.md)
- [ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2](docs/Model/ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2.md)
- [ValidationsApiReportingPeriodsV1PaginatedSubmissions](docs/Model/ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)
- [ValidationsApiReportingPeriodsV1PipelineRun](docs/Model/ValidationsApiReportingPeriodsV1PipelineRun.md)
- [ValidationsApiReportingPeriodsV1PostRequest](docs/Model/ValidationsApiReportingPeriodsV1PostRequest.md)
- [ValidationsApiReportingPeriodsV1PostedResponse](docs/Model/ValidationsApiReportingPeriodsV1PostedResponse.md)
- [ValidationsApiReportingPeriodsV1ReportingPeriodDto](docs/Model/ValidationsApiReportingPeriodsV1ReportingPeriodDto.md)
- [ValidationsApiReportingPeriodsV1ReportingPeriodValidationsRunDto](docs/Model/ValidationsApiReportingPeriodsV1ReportingPeriodValidationsRunDto.md)
- [ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse](docs/Model/ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse.md)
- [ValidationsApiReportingPeriodsV1RunResponse](docs/Model/ValidationsApiReportingPeriodsV1RunResponse.md)
- [ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest](docs/Model/ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest.md)
- [ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequestTypesRecord](docs/Model/ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequestTypesRecord.md)
- [ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest](docs/Model/ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest.md)
- [ValidationsApiReportingPeriodsV1SubmissionCancelledResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionCancelledResponse.md)
- [ValidationsApiReportingPeriodsV1SubmissionListResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionListResponse.md)
- [ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse.md)
- [ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse.md)
- [ValidationsApiReportingPeriodsV1SubmissionMetricsDetails](docs/Model/ValidationsApiReportingPeriodsV1SubmissionMetricsDetails.md)
- [ValidationsApiReportingPeriodsV1SubmissionMetricsResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionMetricsResponse.md)
- [ValidationsApiReportingPeriodsV1SubmissionProfile](docs/Model/ValidationsApiReportingPeriodsV1SubmissionProfile.md)
- [ValidationsApiReportingPeriodsV1SubmissionStatus](docs/Model/ValidationsApiReportingPeriodsV1SubmissionStatus.md)
- [ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse](docs/Model/ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse.md)
- [ValidationsApiReportingPeriodsV1ToggleSelectedRequest](docs/Model/ValidationsApiReportingPeriodsV1ToggleSelectedRequest.md)
- [ValidationsApiReportingPeriodsV1ToggledResponse](docs/Model/ValidationsApiReportingPeriodsV1ToggledResponse.md)
- [ValidationsApiReportingPeriodsV1UpdateBulkRequest](docs/Model/ValidationsApiReportingPeriodsV1UpdateBulkRequest.md)
- [ValidationsApiReportingPeriodsV1UpdateBulkRequestTypesReportingPeriod](docs/Model/ValidationsApiReportingPeriodsV1UpdateBulkRequestTypesReportingPeriod.md)
- [ValidationsApiReportingPeriodsV1UpdatedBulkResponse](docs/Model/ValidationsApiReportingPeriodsV1UpdatedBulkResponse.md)
- [ValidationsApiReportingPeriodsV1ValidationResultRecord](docs/Model/ValidationsApiReportingPeriodsV1ValidationResultRecord.md)
- [ValidationsApiReportingPeriodsV1ValidationSummary](docs/Model/ValidationsApiReportingPeriodsV1ValidationSummary.md)
- [ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId](docs/Model/ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId.md)
- [ValidationsApiReportingPeriodsV1ValidationSummaryCategory](docs/Model/ValidationsApiReportingPeriodsV1ValidationSummaryCategory.md)
- [ValidationsApiReportingPeriodsV1ValidationSummarySubCategory](docs/Model/ValidationsApiReportingPeriodsV1ValidationSummarySubCategory.md)
- [ValidationsApiResultsV1RuleSummary](docs/Model/ValidationsApiResultsV1RuleSummary.md)
- [ValidationsApiRulesV1CreateRequest](docs/Model/ValidationsApiRulesV1CreateRequest.md)
- [ValidationsApiRulesV1PaginatedRules](docs/Model/ValidationsApiRulesV1PaginatedRules.md)
- [ValidationsApiRulesV1RuleDto](docs/Model/ValidationsApiRulesV1RuleDto.md)
- [ValidationsApiRulesV1UpdateRequest](docs/Model/ValidationsApiRulesV1UpdateRequest.md)
- [ValidationsApiRulesV1Url](docs/Model/ValidationsApiRulesV1Url.md)
- [ValidationsApiRulesV1UrlType](docs/Model/ValidationsApiRulesV1UrlType.md)
- [ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse](docs/Model/ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)
- [ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest](docs/Model/ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest.md)
- [ValidationsApiTagsV1CreateRequest](docs/Model/ValidationsApiTagsV1CreateRequest.md)
- [ValidationsApiTagsV1PaginatedTags](docs/Model/ValidationsApiTagsV1PaginatedTags.md)
- [ValidationsApiTagsV1TagDto](docs/Model/ValidationsApiTagsV1TagDto.md)
- [ValidationsApiTagsV1UpdateRequest](docs/Model/ValidationsApiTagsV1UpdateRequest.md)
- [ValidationsApiValidationResultsV1FindResponse](docs/Model/ValidationsApiValidationResultsV1FindResponse.md)
- [ValidationsApiValidationResultsV1ValidationResultDto](docs/Model/ValidationsApiValidationResultsV1ValidationResultDto.md)

## Authorization

Authentication schemes defined for the API:
### oauth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **https://api.edgraph.com/auth/tenant**: EdGraph Platform - Tenant Api

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1.0`
    - Package version: `0.0.44`
    - Generator version: `7.23.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
