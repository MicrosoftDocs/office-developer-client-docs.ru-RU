---
title: Использование CSISyncClient для управления кэша документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэша документов Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399454"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Использование CSISyncClient для управления кэша документов Office (ODC)

Узнайте, как использовать CSISyncClient для управления кэша документов Office (ODC).
  
CSISyncClient является сервером COM ожидания proc (CsiSyncClient.exe), который позволяет Microsoft OneDrive для управления поведением кэша документов Office (ODC). Например OneDrive могут вызывать ODC через CSISyncClient для загрузки файлов в и из конечных точек MS-FSSHTTP включено. Это позволяет расширенных функций резервные службы, в Office, такие как переходы совместного редактирования и полностью из автономного режима для сети.
  
CsiSyncClient доступна в Office Desktop (x86 и x64). Примечание: Во время новых версиях Office может имеющимся в CsiSyncClient, процесс будет использоваться для обеспечения обратной совместимости. Методика управления ODC и интерфейса CsiSyncClient изменится в будущих версиях Office.
  
Идентификатор класса в настоящее время имеет значение только ответить на OneDrive.
  
Можно использовать как сервер ожидания proc COM и выполняется в CsiSyncClient.exe COM-объектов. Из-за ограничения доступа (которая использует ODC) поставляется с типа bit, поступающих Office, поэтому x64 Office означает, что x64 COM-объектом или x86 Office означает, что x86 COM-объектом. Чтобы обойти данное ограничение, определяющее CLSCTX_LOCAL_SERVER как часть CoCreateInstance будет иметь размещаться как сервер COM ожидания proc, позволяя совместимости различной разрядности COM-объектом.
  
## <a name="interfaces"></a>Интерфейсы

CSISyncClient использует следующие интерфейсы.
  
### <a name="interface-ilsclocalsyncclient"></a>Интерфейс ILSCLocalSyncClient

Это основной интерфейс, используемый для синхронизации файлов в Office.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- Библиотека типов: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
COM-объектом, который предоставляется используется как сервер вне процесса. Указание CLSCTX_LOCAL_SERVER как часть CoCreateInstance позволяет совместимости между процессов 32-разрядная и 64-разрядный выпуск.
  
После создания совместного COM-объектом, сначала необходимо вызвать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . После успешного завершения [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) может вызвать любой API часто требуется и в любом порядке. Можно также вызвать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) на уже инициализированный объект, но не выполняет никаких действий. 
  
Исключения в предыдущем параграфе, [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). После вызова [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) на COM-объектом, необходимо удалить этот объект и создать новую. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаление вашей subcache, удалите все сведения о связанных файлов в кэше, но оставить документы на диске. Он также затрагивает состояние для общения с кэшем. Это позволяет вызывать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать новый кэш без необходимости удалить и повторно создать COM-объектом. 
  
**Функции общих элементов**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile используется для удаления файла данных из кэша. Тем не менее этот метод будет закрыто соответствующий файл на диске и на сервере.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, которая идентифицирует Ид_ресурса файла. Это значение должно быть пустым длиной 128 символов. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Заданным Ид_ресурса не находится в кэше.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize не был успешно вызван в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Файл в настоящее время синхронизации или открыть и не может быть удалена.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges Возвращает перечислитель ILSCEvent объекты, а также возвращает маркер, которое задано в следующем вызове GetChanges, при условии, что получатель обработал предыдущей набор событий. События, прежде чем _nPreviousChangesToken_ указан, будут удаленного и недоступен. Если нет событий для обработки, _pnCurrentChangesToken_ должны быть равны значениям _nPreviousChangesToken_, но по-прежнему устанавливающей _ppiEvents_ . 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Параметры

 _nPreviousChangesToken_
  
Определяет, какие события последней обработки потребителем. 
  
 _pnCurrentChangesToken_
  
Идентифицирует самых последних событий затем передаются получателю. Не должно быть значение null.
  
 _ppiEvents_
  
Перечислитель для событий передачи получателю. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission используется для запросов ли Office синхронизации эвристику для сети затрат и энергии переопределяются. На 3G или другую сеть высокая стоимость или при их запуске на батарей сравнение подключен, Office следующим шагом нужно заблокировать сетевого трафика до более opportune времени.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Параметры

 _nspType_
  
Флаг, который определяет какие совет стоимость запроса. В разделе [LSCNetworkSyncPermissionType перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Указывает, в настоящее время переопределен совет запрошенные затраты или нет. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus используется для сбора данных для конкретного файла: является ли он существует в кэше, если у него есть ожидающие обмена данными с копией на сервере, и, если Office 2013 имеет самые даты данных из локальной копии. Требует побитовое флаг [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) значений, чтобы определить, какая информация CsiSyncClient COM-объектом, чтобы запрашивать. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, которая определяет файл на стороне клиента. Это значение должно быть пустым, длиной 128 символов. 
  
 _sfRequestedStatus_
  
Флаг, который определяет, какие сведения для возврата. В разделе [LSCStatusFlag перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Строка, которая определяет расположение файла, определенного _bstrResourceID_ на стороне клиента. Не должно быть значение null. 
  
 _pbstrETag_
  
Строка, которая будет содержать eTag для файл, указанный параметром _bstrResourceID_. Не должно быть значение null. 
  
 _psfFileStatus_
  
Флаг, который будет содержать состояние, при использовании _sfRequestedStatus_ для файл, указанный параметром _bstrResourceID_. Не должно быть значение null. В разделе [LSCStatusFlag перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле, указанного идентификатором _bstrResourceID_ не существует в кэше.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Был запрошен LSCStatusFlag_LocalFileUnchanged или файл, указанный в _bstrResourceID_ заблокированы или отсутствуют.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions возвращает список расширений имени файла с разделителями канала, которые в настоящее время поддерживаются в CsiSyncClient COM-объектом. Обратите внимание на то, что этот список может меняться, и потребитель будет оповещать об изменении с помощью объекта IPartnerActivityCallback, содержащимся на [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (EventOccured см). 
  
Пример строки, возвращаемой выглядит следующим образом: «| docx | docm | pptx |»
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Параметры

 _pbstrSupportedFileExtensions_
  
Строка, должно быть задано набор разделенных вертикальная черта расширения имен файлов, поддерживаемые CsiSyncClient COM-объектом. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize должен быть метод вызывается первым. В противном случае возвращает E_LSC_NOTINITIALIZED другим API. Вызов метода Initialize для уже инициализированный объект возвращает значение S_OK и не имеет никакого эффекта. Если возвращаются E_LSC_CACHEMISMATCH Звонящий может вызвать [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаление кэша, связанного с заданным SuppliedID. Тем не менее в данном случае другие API-интерфейсы по-прежнему возвращает E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Параметры

 _bstrSuppliedID_
  
Определяет потребитель и, для кэширования для использования. Должен быть пустым с 32 знаков. 
  
 _bstrProgID_
  
Определяет COM-объект получателя для двусторонней связи. Должен быть пустым с 39 знаков. Просмотреть [ \<ProgID\> ключ](https://docs.microsoft.com/windows/desktop/com/-progid--key) Дополнительные сведения о коды ProgID. 
  
 _bstrFileSystemDirectoryHint_
  
Определяет корневой каталог, в котором будут храниться локальные файлы. Должен быть пустым с 256 знаков. Каталог уже должен существовать. 
  
 _pEventCallback_
  
Интерфейс обратного вызова, который CsiSyncClient будет уведомление об изменениях. В разделе IPartnerActivityCallback::EventOccurred. Это значение не может быть null. 
  
 _pfCreatedNewCache_
  
Возвращает, был ли создан новый кэш. Если кэширование отключено связан с SuppliedID, он будет создан. Это значение не может быть null.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |SuppliedID уже имеет кэша, связанных с ним, но имеет разные ProgId или FileSystemDirectoryHint отличный от предоставляемых.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (или вложенной папке) уже присутствует в разных кэша.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Программный идентификатор уже присутствует в разных кэша.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange используется CsiSyncClient COM-объектом, чтобы попытаться загрузить указанный файл. Метод подготовить файл для загрузки, включая чтение текущее содержимое файла. Если передаваемых ожидающих установки, предыдущей загрузки будут отменены и отправьте подготовлено для нового содержимого. Если файл открыт для редактирования в приложении, этот метод возвращает значение S_OK без подготовки файл для загрузки (приложение уже делать это действие при наличии изменений).
  
Этот метод позволяет передача если помечено как отправляет заблокированных ранее ( [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)см).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _bstrFileSystemPath_
  
Строка, которая определяет файл на стороне клиента. Это значение должно быть пустым локальный путь с 256 знаков. Этот путь должен быть в дереве каталогов, назначаемое FileSystemDirectoryHint при вызове [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . 
  
 _bstrResourceID_
  
Строка, которая идентифицирует Ид_ресурса файла. Это значение должно быть пустым длиной 128 символов. 
  
 _bstrWebPath_
  
Строка, которая определяет файл на сервере. Это значение должно быть пустым, допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением https://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный в _bstrFileSystemPath_ имеет разные Ид_ресурса не указан. Событие типа LSCEventType_OnFilePathConflict сообщения при этой ошибки. В разделе [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удаленных Среднеатлантическое операции.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Расширение указанного файла не поддерживается объектом CsiSyncClient COM. В разделе [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |COM-объектом собрания не выбрано передаваемых из-за последних изменений с диска файла в кэше.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Файл, указанный в _bstrFileSystemPath_ отсутствует или заблокирован.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный в _bstrResourceID_ имеет разные FileSystemPath не указан.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в различных кэша и еще не могут быть связаны с кэшем получателя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |WebPath предоставляются попадает в разных кэша.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile будет сопоставьте новый URL-адрес и локальный путь для указанного Ид_ресурса. Если файл, указанный в Ид_ресурса еще не существует в кэше, будет предпринята попытка создать его и отметить для загрузки.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Параметры

 _bstrResourceID_
  
Строка, которая идентифицирует Ид_ресурса файла. Это значение должно быть пустым длиной 128 символов. 
  
 _bstrNewFileSystemPath_
  
Строка, которая задает новый локальный путь для файла. Это значение должно быть пустым локальный путь с 256 знаков. Этот путь должен быть в дереве каталогов, указанный с FileSystemDirectoryHint, когда вызов для инициализации. 
  
 _bstrNewWebPath_
  
Строка, которая задает новый URL-адрес для файла. Это значение должно быть пустым допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением https://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Указывает, разрешены ли в настоящее время отправки в новом месте. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ или _bstrNewWebPath_ уже существует на другой файл в любой кэш. Событие типа LSCEventType_OnFilePathConflict сообщения при этой ошибки. В разделе [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле был удален из кэша во время выполнения этого метода.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Файл, указанный в настоящее время синхронизации в приложении Microsoft Office.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache приведет к удалению кэша, связанного с SuppliedID, которое было указано на Initialize. Это включает в себя все сведения о файле, но останется файлов на клиенте и на сервере. Этот метод также оставляет объект в частично не инициализированный состоянии. Вызовы допустимо только после этого — это [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Этот метод может вызываться при инициализации, возникает ошибка и возвращает E_LSC_CACHEMISMATCH и приведет к удалению кэша, связанного с SuppliedID, которое было указано при вызове со сбоями.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Параметры

None
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызывается в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange указывает CsiSyncClient COM-объектом, чтобы пометить указанный файл для загрузки. Если файл открыт в приложении Microsoft Office для изменения, этот метод возвращает значение S_OK не помечая файл для загрузки (приложение уже делать это действие при наличии изменений).
  
Этот метод позволяет загрузки если помечено как файлы для загрузки заблокированных ранее (RenameFile см).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

|Параметр|Описание|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Строка, которая определяет файл на стороне клиента. Это значение должно быть пустым локальный путь с 256 знаков. Этот путь должен быть в дереве каталогов, указанный с FileSystemDirectoryHint, когда вызов для инициализации.  <br/> |
|bstrResourceID  <br/> |Строка, которая идентифицирует Ид_ресурса файла. Это значение должно быть пустым длиной 128 символов.  <br/> |
|bstrWebPath  <br/> |Строка, которая определяет файл на сервере. Это значение должно быть пустым допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при попытке подключения к состояние кэша.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный в _bstrFileSystemPath_ имеет разные Ид_ресурса не указан.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Расширение указанного файла не поддерживается объектом CsiSyncClient COM. В разделе GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в середине операции.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный в _bstrResourceID_ имеет разные FileSystemPath не указан.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в различных кэша и еще не могут быть связаны с кэшем получателя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |WebPath предоставляются попадает в разных кэша.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Задает кэш в автономном и интерактивном состояние. Если в автономном режиме, Office не будет пытаться связаться с сервером для всех файлов в этом кэше, независимо от настройки _fBlockUploads_ каждого отдельного файла. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Параметры

 _fIsOnline_
  
Логическое значение, определение состояния подключения кэша. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при попытке подключения к состояние кэша.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission используется для переопределять или restoreOffice's синхронизации эвристику для сети затрат и power об использовании. На 3G или другую сеть высокая стоимость или при их запуске на батарей сравнение подключен, Office следующим шагом нужно заблокировать сетевого трафика до более opportune времени. Потребитель этот интерфейс API можно использовать для переопределения эвристику Office и Принудительная синхронизация будет выполнена.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Параметры

 _nspType_
  
Флаг, который определяет, какие расходы Совет для переопределения. В разделе [LSCNetworkSyncPermissionType перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Указывает, следует ли для принудительной синхронизации на таким образом переопределение этот совет затраты или больше не переопределить его. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой, связанный с переопределить синхронизации эвристику.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Выгрузка кэша из объекта COM и выполнять операции закрытия. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) НЕОБХОДИМО вызывать перед удалением COM-объектом. После вызова можно вызвать другие интерфейсы API, должен быть потеряны COM-объектом и создан новый, если продолжить выполнение операции. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при выполнении отмены инициализации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Интерфейс IEnumLSCEvent

Этот интерфейс представляет список событий ILSCEvent.
  
**Функции общих элементов**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Возвращает следующее событие из списка событий.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Параметры

 _ppiLSCEvent_
  
Указатель на интерфейс ILSCEvent.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Нет дополнительных событий.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Сбрасывает перечислитель для первого события.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
### <a name="interface-ilscevent"></a>Интерфейс ILSCEvent

Этот интерфейс представляет событие синхронизации. Все сведения о событии могут быть получены из интерфейса.
  
**Функции общих элементов**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Обратите внимание на то, что это значение заполняется при [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) вызывается, не в том случае, когда событие был создан, поэтому будут иметь только текущее состояние файла не состояние файла при изменении состояния конфликта. 
  
Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Параметры

 _pfIsInConflict_
  
Текущее состояние конфликта файла, связанный с событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Параметры

 _pnError_
  
Ошибка, связанный с данным событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Параметры

 _pbstrETag_
  
ETag, связанный с данным событием
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Получает тип для этого события.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Параметры

 _pnEventType_
  
Тип события это событие. В разделе [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) допустимые значения. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Возвращает локальный путь рабочее для этого события.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Параметры

 _pbstrLocalWorkingPath_
  
Локальный путь к файлу, к которому относится это событие. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Получает идентификатор ресурсов для события.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Параметры

 _pbstrResourceID_
  
Ид_ресурса файла, связанного с данным событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. Когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызовет конфликт Web или локальный путь с другой файл кэша файлов Office, это генерируется событие. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Параметры

 _pbstrResourceIDAttempted_
  
Ид_ресурса, вызвавшего это событие, чтобы получить созданные. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Параметры

 _pnSyncErrorType_
  
Тип ошибки, связанный с данным событием. В разделе [LSCEventType перечисление](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) возможных значений. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Параметры

 _pbstrWebPath_
  
Указывает веб-путь, связанный с данным событием. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK. 
  
### <a name="interface-ilscevent2"></a>Интерфейс ILSCEvent2

Этот интерфейс содержит дополнительные сведения о синхронизации событий.
  
**Функции общих элементов**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Получает сведения об ошибке цепочки о синхронизации событий.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Параметры

 _pbstrErrorChain_
  
Строка для хранения цепочки сведения об ошибке. Не должно быть значение null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_NOTIMPL  <br/> |Установленная версия Office не поддерживает этот интерфейс  <br/> |
|E_INVALIDARG  <br/> |Одно или несколько значений параметров являются недопустимыми.  <br/> |
|E_FAIL  <br/> |Сведения об ошибке цепочки недоступен.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Интерфейс IPartnerActivityCallback

Этот интерфейс предоставляет функцию обратного вызова для CSISyncClient COM-объектом.
  
**Функции общих элементов**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Это функции обратного вызова на объект, заданный для CsiSyncClient COM-объектом. Предполагается, что при возникновении события (разделе [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) допустимых типов событий), CsiSyncClient COM-объектом будут вызывать этот метод, сигналов потребителем. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Параметры

 _eEventTypeOccurred_
  
Тип события это событие. В разделе [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) допустимые значения. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает значение S_OK.
  
## <a name="enumerations"></a>Перечисления

CSISyncClient использует следующие перечисления.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Это перечисление определяет категории ошибок, которые могут возникнуть во время синхронизации в файл.
  
|Перечислитель|Описание|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Ошибка синхронизации для этого события непредвиденное и может потребоваться особое внимание. По умолчанию пользователь может иметь предотвратить.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Ошибка синхронизации для этого события не обязательно особое внимание. Office будет обрабатывать его автоматически.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Ошибка синхронизации для этого события требуется пользователя ее решения. Ошибка конфликта объединения требуется пользователя для открытия документа и слияние его.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Потребитель предотвратить, требует синхронизации ошибки это событие, но не требуют особое внимание пользователем.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Ошибка синхронизации для этого события требуется потребитель предотвратить как особый случай.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Это перечисление указывает тип события, которые могут возникнуть для определенного файла.
  
|Перечислитель|Описание|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Изменения были внесены в локальный файл.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Пользователь может открыть файл.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Завершения загрузки изменений в файле с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Отправка изменений в файле на сервере завершена.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Состояние конфликта объединения файла был изменен.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Файл был добавлен.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Файл был удален.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Синхронизация была включена поддержка файлы пользователя.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Начало загрузку изменений в файле с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Первые шаги в отправке изменений в файле на сервер.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Это событие создается при вызове [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) приводит к возникновению конфликта Web или локальный путь с другой файл в Кэш файлов Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Это перечисление указывает тип события, которые могут возникнуть. Он должен вызова определенных функций ILSCLocalSyncClient на основе типа события.
  
|Перечислитель|Описание|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Произошла ILSCEvent. Пользователь должен вызвать [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для извлечения данных.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Расширения имен файлов, поддерживаемые были изменены. Пользователь должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) получить новый список поддерживаемых расширений.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Это перечисление указывает флаги, используемые для совет стоимость сети. 

|Перечислитель|Описание|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |Значение true, если совет стоимость дорогостоящих сетей (например, 3 G) имеет преимущество.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |Значение true, если совет затрат для использования power (например, батарей) имеет преимущество.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Это перечисление используется для представления состояния синхронизации файла. 
  
|Перечислитель|Описание|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |Значение true, если ожидает данных для отправки в файл сервера.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |Значение true, если ожидает данных для загрузки из файла сервера.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |Значение true, если данные Office на файл в кэш последнюю копию данных на диске.  <br/> |
   

