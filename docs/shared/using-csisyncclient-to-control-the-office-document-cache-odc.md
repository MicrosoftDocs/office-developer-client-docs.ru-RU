---
title: Использование CSISyncClient для управления кэшом документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэшом документов Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Использование CSISyncClient для управления кэшом документов Office (ODC)

Узнайте, как использовать CSISyncClient для управления кэшом документов Office (ODC).
  
CSISyncClient — это сервер COM, который не является прокси-сервером (CsiSyncClient.exe), который позволяет Microsoft OneDrive управлять поведением кэша документов Office (ODC). Например, OneDrive может вызвать ODC через CSISyncClient для отправки и загрузки файлов в конечные точки с поддержкой MS-FSSHTTP и из них. Это позволяет использовать расширенные функции Office с помощью службы, такие как совместное авторство и плавный переход от автономного к сетевому.
  
CsiSyncClient доступен в Office Desktop (x86 и x64). Примечание. Хотя более новые версии Office могут быть погрузки с помощью CsiSyncClient, этот процесс будет использоваться только для обратной совместимости. Интерфейс CsiSyncClient и методология управления ODC изменятся в будущих версиях Office.
  
В настоящее время этот ИД класса настроен для ответа только на OneDrive.
  
Com-объект может быть заархивируемым com-сервером и работает в CsiSyncClient.exe. Из-за ограничений Access (который использует ODC), он поставляется с типом бита, в который входит Office, поэтому x64 Office означает объект x64 COM, а x86 Office — объект COM x86. Чтобы обойти это ограничение, при указании CLSCTX_LOCAL_SERVER как части CoCreateInstance com-объект будет иметь место как сервер COM, который не является сервером COM, что обеспечивает совместимость между битами.
  
## <a name="interfaces"></a>Интерфейсы

CSISyncClient использует следующие интерфейсы.
  
### <a name="interface-ilsclocalsyncclient"></a>Интерфейс ILSCLocalSyncClient

Это основной интерфейс, используемый для синхронизации файлов в Office.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Объект COM, который выставит, используется в качестве вне proc-сервера. Указание CLSCTX_LOCAL_SERVER как части CoCreateInstance позволяет совместить процессы от 64 до 32 раз.
  
После создания объекта COM необходимо сначала вызвать [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) После [успешного завершения ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) любой API можно вызывать как можно чаще и в любом порядке. Также можно вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) для уже инициализированного объекта, но это ничего не делает. 
  
Исключениями из предыдущего абзаца являются [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). После вызова [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) объекта COM необходимо уничтожать этот объект и создавать новый. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удалит ваш подкаш, удалит все связанные сведения о файле в кэше, но оставляет документы на диске. Оно также оставляет состояние без изменений для связи с кэшом. Это позволяет вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать кэш без необходимости уничтожения и воссоздания com-объекта. 
  
**Функции открытых членов**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile используется для удаления сведений о файле из кэша. Однако этот метод оставляет связанный файл на диске и на сервере.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, идентифицирует ResourceID файла. Это значение должно быть непустым и иметь не более 128 символов. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Заданный ResourceID не находится в кэше.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Инициализация не была успешно вызвана в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |В настоящее время файл синхронизируется или открывается и не может быть удален.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges возвращает enumerator объектов ILSCEvent, а также возвращает маркер, который передается следующему вызову GetChanges, если потребитель обработал предыдущий набор событий. События перед  _указанным nPreviousChangesToken_ будут удалены и недоступны. Если обработка событий не происходит,  _pnCurrentChangesToken_ должен иметь то же значение, что  _и nPreviousChangesToken,_ но  _ppiEvents_ все равно будет установлен. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Параметры

 _nPreviousChangesToken_
  
Определяет, какое событие было обработано потребителем в последний раз. 
  
 _pnCurrentChangesToken_
  
Определяет последнее событие, которое передается потребителю. Не должно быть null.
  
 _ppiEvents_
  
Enumerator для событий, переданных потребителю. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission используется для запроса на необходимость переопределения синхронизации office с использованием сетевой стоимости и энергопотребления. Если в сети с высокой стоимостью 3G или в сети с высокой стоимостью либо при работе от аккумулятора или при подключении к сети, Office может заблокировать сетевой трафик до более непрозраченного времени.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Параметры

 _nspType_
  
Флаг, определяющий, какие затраты необходимо запросить. См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType) 
  
 _pfSyncEnabled_
  
Указывает, переопределяется ли в настоящее время запросивая авристическая стоимость. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus используется для сбора сведений об определенном файле: существует ли он в кэше, находится ли в состоянии ожидания связь с копией сервера и есть ли в Office 2013 самые последние данные из локальной копии. Для определения сведений, запрашиваемой COM-объектом CsiSyncClient, требуется битовая пометка значений [Enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, идентифицирует файл в клиенте. Это значение должно быть непустым и иметь не более 128 символов. 
  
 _sfRequestedStatus_
  
Флаг, который определяет возвращаемую информацию. См. [enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 
  
 _pbstrFileSystemPath_
  
Строка, которая определяет расположение файла, определяемого  _bstrResourceID_ в клиенте. Не должно быть null. 
  
 _pbstrETag_
  
Строка, которая будет содержать eTag для файла, заданного _bstrResourceID._ Не должно быть null. 
  
 _psfFileStatus_
  
Флаг, который будет содержать состояние, запрашиваемого  _с помощью sfRequestedStatus_ для файла, заданного  _bstrResourceID_. Не должно быть null. См. [enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле, указанные  _bstrResourceID,_ не существуют в кэше.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged запроса или файл, указанный  _bstrResourceID,_ заблокирован или отсутствует.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions возвращает список расширений файлов, которые в настоящее время поддерживаются com-объектом CsiSyncClient. Обратите внимание, что этот список может измениться, и потребитель получит уведомление об изменении с помощью объекта IPartnerActivityCallback, предоставленного в [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (См. EventOccured). 
  
Пример возвращаемой строки: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Параметры

 _pbstrSupportedFileExtensions_
  
Строка, устанавливаемая с помощью набора расширений файлов, которые поддерживаются com-объектом CsiSyncClient. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Инициализация должна быть первым вызванным методом. В противном случае все остальные API будут возвращать E_LSC_NOTINITIALIZED. Вызов инициализации для уже инициализированного объекта S_OK и ничего не делает. Если E_LSC_CACHEMISMATCH возвращается, вызываемая может вызвать [ILSCLocalSyncClient::ResetCache, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) чтобы удалить кэш, связанный с данным SuppliedID. Однако в этом случае другие API по-прежнему будут возвращать E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Параметры

 _bstrSuppliedID_
  
Определяет потребителя и кэш для использования. Должен быть непустым и иметь не более 32 символов. 
  
 _bstrProgID_
  
Определяет COM-объект потребителя для двунабной связи. Должен быть непустым и иметь не более 39 символов. Дополнительные [ \< сведения \> о progID](https://docs.microsoft.com/windows/desktop/com/-progid--key) см. в ключе ProgID. 
  
 _bstrFileSystemDirectoryHint_
  
Определяет корневой каталог, в котором будут храниться локальные файлы. Должен быть непустым и иметь не более 256 символов. Каталог должен уже существовать. 
  
 _pEventCallback_
  
Интерфейс callback, который CsiSyncClient будет уведомлять об изменениях. См. IPartnerActivityCallback::EventOccurred. Это значение не должно иметь значение NULL. 
  
 _pfCreatedNewCache_
  
Возвращает, был ли создан новый кэш. Если с SuppliedID кэш не связан, он будет создан. Это значение не должно иметь значение NULL.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |С ним уже связан кэш SuppliedID, но он отличается от предоставленного progId или FileSystemDirectoryHint.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (или вузаная папка) уже существует в другом кэше.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |ProgID уже существует в другом кэше.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange используется для отправки указанного файла объекту COM CsiSyncClient. Метод подготовит файл к отправке, включая чтение текущего содержимого файла. Если отправка уже ожидает отправки, предыдущая отправка будет отклонена, а новое содержимое будет подготовлено к отправке. Если файл открыт для редактирования в приложении, этот метод возвращает S_OK без подготовки файла к отправке (приложение должно уже сделать это при внесении изменений).
  
Этот метод разрешает отправку, если он был помечен как ранее заблокированный (см. [ILSCLocalSyncClient::RenameFile). ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _bstrFileSystemPath_
  
Строка, идентифицирует файл в клиенте. Это значение должно быть непустым локальным путем не более 256 символов. Этот путь должен быть в дереве каталогов, заданном FileSystemDirectoryHint при вызове [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) 
  
 _bstrResourceID_
  
Строка, идентифицирует ResourceID файла. Это значение должно быть непустым и иметь не более 128 символов. 
  
 _bstrWebPath_
  
Строка, идентифицирует файл на сервере. Это значение должно быть непустым, допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 . 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указано. Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки. См. [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в середине операции.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Заданное расширение файла не поддерживается com-объектом CsiSyncClient. См. [ILSCLocalSyncClient::GetSupportedFileExtensions. ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Com-объект не запланил отправку, так как файл в кэше имел последние изменения с диска.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Файл, указанный  _bstrFileSystemPath,_ отсутствует или заблокирован.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный  _bstrResourceID,_ имеет файл FileSystemPath, который отличается от указанного.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в другом кэше и еще не может быть связан с кэшом потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Предоставленный WebPath попадает в другой кэш.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile связывает новый URL-адрес и локальный путь для заданного ResourceID. Если файл, указанный с помощью ResourceID, еще не существует в кэше, будет предпринята попытка создать его и пометить для скачивания.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, идентифицирует ResourceID файла. Это значение должно быть непустым и иметь не более 128 символов. 
  
 _bstrNewFileSystemPath_
  
Строка, которая указывает новый локальный путь к файлу. Это значение должно быть непустым локальным путем не более 256 символов. Этот путь должен быть указан в дереве каталогов, указанном FileSystemDirectoryHint при вызове инициализации. 
  
 _bstrNewWebPath_
  
Строка, которая указывает новый URL-адрес файла. Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 . 
  
 _fBlockUploads_
  
Указывает, разрешены ли в данный момент отправки в новое расположение. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ или _bstrNewWebPath уже_ существуют в другом файле в любом кэше. Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки. См. [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле были удалены из кэша во время работы этого метода.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл в настоящее время синхронизируется в приложении Office.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache удалит кэш, связанный с SuppliedID, предоставленным при инициализации. К ним относятся все сведения о файле, но файлы будут оставляться как на клиенте, так и на сервере. Этот метод также оставляет объект в частично неинициализированном состоянии. После этого единственными допустимыми вызовами [являются ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize. ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Этот метод МОЖЕТ вызываться, если инициализация не удалась и возвращает E_LSC_CACHEMISMATCH и удаляет кэш, связанный с SuppliedID, который был предоставлен при сбое вызова.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Параметры

Нет
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange сообщает COM-объекту CsiSyncClient пометить указанный файл для скачивания. Если файл открыт в приложении Office для редактирования, этот метод возвращает S_OK без пометки файла для скачивания (приложение должно уже сделать это при внесении изменений).
  
Этот метод разрешает скачивание, если он был помечен как скачиваемые ранее заблокированные (см. renameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

|Параметр|Описание|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Строка, идентифицирует файл в клиенте. Это значение должно быть непустым локальным путем не более 256 символов. Этот путь должен быть указан в дереве каталогов, указанном FileSystemDirectoryHint при вызове инициализации.  <br/> |
|bstrResourceID  <br/> |Строка, идентифицирует ResourceID файла. Это значение должно быть непустым и иметь не более 128 символов.  <br/> |
|bstrWebPath  <br/> |Строка, идентифицирует файл на сервере. Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .  <br/> |
   
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при настройках состояния подключения к кэше.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указано.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Заданное расширение файла не поддерживается com-объектом CsiSyncClient. См. getSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в середине операции.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный  _bstrResourceID,_ имеет файл FileSystemPath, который отличается от указанного.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в другом кэше и еще не может быть связан с кэшом потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Предоставленный WebPath попадает в другой кэш.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Устанавливает кэш в сетевое или автономное состояние. В автономном режиме Office не будет пытаться связаться с сервером для файлов в этом кэше, независимо от настроек  _fBlockUploads_ каждого отдельного файла. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Параметры

 _fIsOnline_
  
Boolean, определяющее состояние подключения кэша. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при настройках состояния подключения к кэше.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission используется для переопределения или восстановления синхронизированной heuristicsOffice для затрат на сеть и использования питания. Если в сети с высокой стоимостью 3G или в сети с высокой стоимостью либо при работе от аккумулятора или при подключении к сети, Office может заблокировать сетевой трафик до более непрозраченного времени. Потребитель этого API может использовать его для переопределения ауристических действий Office и принудительной синхронизации.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Параметры

 _nspType_
  
Флаг, который определяет, какие затраты переопределять. См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)
  
 _fEnableSync_
  
Указывает, следует ли принудительно синхронизироваться, переопределив эту ауристическую стоимость, или больше не переопределять ее. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Невыполнение переопределения синхронизации с ауристией.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Выгружает кэш из объекта COM и выполняет операции закрытия. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) ДОЛЖЕН быть вызван перед уничтожением com-объекта. После этого никакие другие API не могут быть вызваны, com-объект ДОЛЖЕН быть уничтожен и создан новый, если вы хотите продолжить работу. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой uninitialize.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Интерфейс IEnumLSCEvent

Этот интерфейс представляет список событий ILSCEvent.
  
**Функции открытых членов**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Извлекает следующее событие из списка событий.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Параметры

 _ppiLSCEvent_
  
Указатель на интерфейс ILSCEvent.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Больше нет событий.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Сбрасывает enumerator до первого события.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent"></a>Интерфейс ILSCEvent

Этот интерфейс представляет событие синхронизации. Все сведения о событии можно получить из интерфейса.
  
**Функции открытых членов**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Обратите внимание, что это значение заполняется при вызвании [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) а не при его добавлении, поэтому при смене состояния конфликта у вас будет только текущее состояние файла, а не его состояние. 
  
Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Параметры

 _pfIsInConflict_
  
Текущее состояние конфликта файла, связанного с событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Параметры

 _pnError_
  
Ошибка, связанная с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Параметры

 _pbstrETag_
  
ETag, связанный с этим событием
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Получает тип для этого события.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Параметры

 _pnEventType_
  
Тип события этого события. Допустимые значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Получает локальный рабочий путь для этого события.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Параметры

 _pbstrLocalWorkingPath_
  
Локальный путь к файлу, к которому относится это событие. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Получает ИД ресурса для события.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Параметры

 _pbstrResourceID_
  
ResourceID файла, связанного с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. Когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) приведет к конфликту веб-пути или локального пути с другим файлом в кэше файлов Office, создается это событие. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Параметры

 _pbstrResourceIDAttempted_
  
ResourceID, который вызвал это событие для получения. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Параметры

 _pnSyncErrorType_
  
Тип ошибки, связанный с этим событием. Возможные значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров недопустимы.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Параметры

 _pbstrWebPath_
  
Указывает веб-путь, связанный с этим событием. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent2"></a>Интерфейс ILSCEvent2

Этот интерфейс содержит дополнительные сведения о событии синхронизации.
  
**Функции открытых членов**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Получает сведения о цепочке ошибок о событии синхронизации.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Параметры

 _pbstrErrorChain_
  
Строка для удержания сведений о цепочке ошибок. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_NOTIMPL  <br/> |Установленная версия Office не поддерживает этот интерфейс  <br/> |
|E_INVALIDARG  <br/> |Одно или несколько значений параметров являются недопустимыми.  <br/> |
|E_FAIL  <br/> |Сведения о цепочке ошибок недоступны.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Интерфейс IPartnerActivityCallback

Этот интерфейс предоставляет функцию вызова объекту COM CSISyncClient.
  
**Функции открытых членов**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Это функция вызова для объекта, заданного объекту CsiSyncClient COM. Ожидается, что при событии (см. [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) COM-объект CsiSyncClient будет вызывать этот метод, сигнализировать потребителя. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Параметры

 _eEventTypeOccurred_
  
Тип события этого события. Допустимые значения см. в [enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK.
  
## <a name="enumerations"></a>Перечисления

CSISyncClient использует следующие enumerations.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Это enumeration указывает категории ошибок, которые могут возникнуть при синхронизации файла.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Ошибка синхронизации этого события была непредвиденная и может потребовать особого внимания. По умолчанию пользователю может потребоваться вмешательство.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Ошибка синхронизации этого события не требует особого внимания. Office будет обрабатывать его автоматически.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Ошибка синхронизации этого события требует от пользователя ее устранения. Например, при объединении с конфликтом пользователь должен открыть документ и объединить его.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Ошибка синхронизации этого события требует вмешательства потребителя, но не требует особого внимания пользователя.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Ошибка синхронизации этого события требует, чтобы потребитель вступил в особый случай.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Это значение указывает тип событий, которые могут произойти для конкретного файла.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |В локальный файл были внесены изменения.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Пользователь открыл файл.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Загрузка изменений файлов с сервера завершена.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Отправка изменений файлов на сервер завершена.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Состояние конфликта объединения файла изменилось.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Добавлен файл.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Файл был удален.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Синхронизация включена для файлов пользователя.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Начал скачивать изменения файлов с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Началась отправка изменений файлов на сервер.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Это событие создается, когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает конфликт веб-пути или локального пути с другим файлом в кэше файлов Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Это enumeration указывает тип событий, которые могут произойти. Потребителю необходимо вызывать определенные функции ILSCLocalSyncClient в зависимости от типа события.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Произошел ilSCEvent. Потребитель должен вызвать [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для получения данных.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Поддерживаемые расширения файлов изменились. Потребитель должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) чтобы получить новый список поддерживаемых расширений.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Это enumeration specifies the flags used for a network cost heuristic. 

|Enumerator|Описание|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |Имеет true, если переопределяется дорожная выгружаемая стоимость для дорогостоящих сетей (например, 3G).  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |Имеет true, если переопределяется побороть затраты на использование питания (например, аккумулятор).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Это enumeration используется для представления состояния синхронизации файла. 
  
|Enumerator|Описание|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |Имеет true, если в файле сервера есть ожидающих данных.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |Имеет true, если есть ожидающих загрузки данных из файла сервера.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |Имеет true, если данные, хранимые в файле в кэше Office, — это самая новейшая копия данных на диске.  <br/> |
   

