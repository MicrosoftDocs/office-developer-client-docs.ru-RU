---
title: Использование CSISyncClient для управления кэшом Office документов (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэшом Office документов (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Использование CSISyncClient для управления кэшом Office документов (ODC)

Узнайте, как использовать CSISyncClient для управления кэшом Office документов (ODC).
  
CSISyncClient — это сервер com(CsiSyncClient.exe), который позволяет Microsoft OneDrive управлять поведением кэша документов Office (ODC). Например, OneDrive может вызвать ODC через CSISyncClient для загрузки файлов в конечные точки с включенной поддержкой MS-FSSHTTP и из нее. Это позволяет использовать расширенные функции, Office службы, такие как совместное авторство и бесшовные переходы из автономного в online.
  
CsiSyncClient доступен в Office Desktop (как x86, так и x64). Примечание. Хотя более новые версии Office могут быть отгрузка с CsiSyncClient, этот процесс будет использоваться только для обратной совместимости. Интерфейс CsiSyncClient и методология управления ODC изменятся в будущих версиях Office.
  
В настоящее время ID класса должен отвечать только на OneDrive.
  
Объект COM может быть угодным в качестве неугодного com-сервера и выполняется в CsiSyncClient.exe. Из-за ограничений с Access (который использует ODC), он поставляется с типом бита, который Office входит, поэтому x64 Office означает объект x64 COM, или x86 Office означает объект x86 COM. Чтобы обойти это ограничение, укажите CLSCTX_LOCAL_SERVER в качестве части CoCreateInstance будет иметь объект COM, который будет иметь возможность использовать com-сервер, который не является профессиональным com-сервером, что обеспечивает совместимость между битами.
  
## <a name="interfaces"></a>Интерфейсы

CSISyncClient использует следующие интерфейсы.
  
### <a name="interface-ilsclocalsyncclient"></a>Интерфейс ILSCLocalSyncClient

Это основной интерфейс, используемый для синхронизации файлов в Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Объект COM, который подвергается воздействию, используется в качестве неавтономного сервера. Указание CLSCTX_LOCAL_SERVER в составе CoCreateInstance позволяет совмесить между процессами 64bit и 32bit.
  
После совместной создания объекта COM необходимо сначала вызвать [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) После успешного завершения [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) любой API можно вызывать так часто, как вы хотите и в любом порядке. Вы также можете вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) на уже инициализированном объекте, но это ничего не делает. 
  
Исключения из предыдущего абзаца: [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). После вызова [ОБЪЕКТА ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) на объекте COM необходимо уничтожить этот объект и создать новый. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаляет подкаченик, удаляет все связанные сведения о файле в кэше, но оставляет документы на диске. Он также оставляет состояние нетронутым для связи с кэшом. Это позволяет вызвать [ILSCLocalSyncClient:::Initialize, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) чтобы создать новый кэш без необходимости уничтожения и воссоздания объекта COM. 
  
**Функции общедоступных членов**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile используется для удаления данных файлов из кэша. Однако этот метод оставит связанный файл на диске и на сервере.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Строка, определяемая ResourceID файла. Это значение должно быть непустым с максимальным значением 128 символов. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Данный ResourceID не находится в кэше.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize не была успешно вызвана в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |В настоящее время файл синхронизируется или открыт и не может быть удален.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges возвращает объекты ILSCEvent, а также возвращает маркер, который будет передан следующему вызову в GetChanges, если предположить, что потребитель обработал предыдущий набор событий. События перед  _указанным nPreviousChangesToken_ будут удалены и недоступны. Если события не будут обработаны,  _pnCurrentChangesToken_ должен иметь то же значение, что  _и nPreviousChangesToken,_ но  _ppiEvents_ все равно будет задат. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameters

 _nPreviousChangesToken_
  
Определяет, какое событие в последний раз обрабатывалось потребителем. 
  
 _pnCurrentChangesToken_
  
Определяет последнее событие, переданное потребителю. Не должно быть null.
  
 _ppiEvents_
  
Переумывчик событий, переданных потребителю. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission используется для запроса, Office ли Office синхронизации с сетевыми затратами и использованием электроэнергии. При работе с 3G или другой дорогостояной сетью или при работе с аккумулятором в сравнении с подключением Office может заблокировать сетевой трафик до более подходящих периодов времени.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Флаг, определяющий, какие затраты на запрос. См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType) 
  
 _pfSyncEnabled_
  
Указывает, переопределена ли в настоящее время запрашиваемая еуристическая стоимость. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus используется для сбора сведений для определенного файла: существует ли он в кэше, имеет ли он ожидающих связи с копией сервера и если Office 2013 г. имеет самые последние данные из локальной копии. Для определения того, для каких сведений запрашивается объект CsiSyncClient COM, требуется флаг [Enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Строка, определяемая файлом клиента. Это значение должно быть не пустым, а не более 128 символов. 
  
 _sfRequestedStatus_
  
Флаг, который определяет, какие сведения нужно возвращать. См. [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Строка, которая определяет расположение файла, определяемого  _bstrResourceID_ на клиенте. Не должно быть null. 
  
 _pbstrETag_
  
Строка, которая будет содержать eTag для файла, идентифицированного _bstrResourceID._ Не должно быть null. 
  
 _psfFileStatus_
  
Флаг, который будет содержать состояние, запрашиваемого _с помощью sfRequestedStatus_ для файла, идентифицированного _bstrResourceID._ Не должно быть null. См. [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файлах, указанные  _bstrResourceID,_ не существуют в кэше.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged запросили или файл, указанный  _bstrResourceID,_ заблокирован или отсутствует.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions возвращает список расширений файлов, которые в настоящее время поддерживаются объектом CsiSyncClient COM. Обратите внимание, что этот список может измениться, и потребитель будет уведомлен об изменении с помощью объекта IPartnerActivityCallback, предоставленного в [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (см. eventOccured). 
  
Пример возвращаемой строки: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameters

 _pbstrSupportedFileExtensions_
  
Строка, которая должна быть установлена с набором расширений файлов, поддерживаемых объектом CsiSyncClient COM. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Инициализация должна быть первым вызванным методом. В противном случае все другие API возвращаются E_LSC_NOTINITIALIZED. Вызов Initialize на уже инициализированном объекте возвращает S_OK и ничего не делает. Если E_LSC_CACHEMISMATCH возвращается, вызываемая может вызвать [ILSCLocalSyncClient::ResetCache, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) чтобы удалить кэш, связанный с данным SuppliedID. Однако в этом случае другие API все равно будут возвращать E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameters

 _bstrSuppliedID_
  
Определяет потребителя и какой кэш использовать. Должно быть непустым с максимальной 32 символами. 
  
 _bstrProgID_
  
Определяет объект COM потребителя для двуна пути связи. Должно быть непустым с максимумом 39 символов. Дополнительные сведения о progID-данных см. в [ \< \> progID-ключе.](https://docs.microsoft.com/windows/desktop/com/-progid--key) 
  
 _bstrFileSystemDirectoryHint_
  
Определяет корень каталога, в котором будут храниться локальные файлы. Должно быть непустым с максимальным значением 256 символов. Каталог уже должен существовать. 
  
 _pEventCallback_
  
Интерфейс вызова, который CsiSyncClient уведомит об изменениях. См. iPartnerActivityCallback::EventOccurred. Это значение не должно быть null. 
  
 _pfCreatedNewCache_
  
Возвращает, был ли создан новый кэш. Если кэш не связан с SuppliedID, он будет создан. Это значение не должно быть null.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |В SuppliedID уже есть кэш, связанный с ним, но он отличается от предоставляемых ProgId или FileSystemDirectoryHint.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Файл FileSystemDirectoryHint (или поддвектор) уже существует в другом кэше.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |ProgID уже существует в другом кэше.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange используется для отправки указанного файла в объект CsiSyncClient COM. Метод подготовит файл к отправке, включая чтение текущего содержимого файла. Если отправка уже не завершена, предыдущая загрузка будет отброшена и новое содержимое будет подготовлено к отправке. Если файл открыт для редактирования в приложении, этот метод возвращается S_OK без подготовки файла к отправке (приложение уже должно сделать этот шаг, если есть изменения).
  
Этот метод позволит загружать, если он был отмечен как заблокированные ранее загрузки (см. [ilSCLocalSyncClient::RenameFile). ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrFileSystemPath_
  
Строка, идентифицируемая с файлом клиента. Это значение должно быть непустым локальным путем с максимальным значением 256 символов. Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове [в ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) 
  
 _bstrResourceID_
  
Строка, определяемая ResourceID файла. Это значение должно быть непустым с максимальным значением 128 символов. 
  
 _bstrWebPath_
  
Строка, идентифицирует файл на сервере. Это значение должно быть непустым, допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 . 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указанный. Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки. См. [ilSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в середине операции.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Заданное расширение файла не поддерживается объектом CsiSyncClient COM. См. [ilSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Объект COM не запланировать отправку, так как в файле кэша произошли самые последние изменения с диска.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Файл, указанный  _bstrFileSystemPath,_ отсутствует или заблокирован.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный  _bstrResourceID,_ отличается от указанного файла FileSystemPath.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в другом кэше и пока не может быть связан с кэшом потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Предоставляемый ВебПат попадает под другой кэш.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile будет связывать новый URL-адрес и локальный путь для данного ResourceID. Если файл, указанный ResourceID, еще не существует в кэше, будет предпринята попытка создать его и пометить его для скачивания.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Строка, определяемая ResourceID файла. Это значение должно быть непустым с максимальным значением 128 символов. 
  
 _bstrNewFileSystemPath_
  
Строка, которая указывает новый локальный путь для файла. Это значение должно быть непустым локальным путем с максимальным значением 256 символов. Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове инициализации. 
  
 _bstrNewWebPath_
  
Строка, которая указывает новый URL-адрес файла. Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 . 
  
 _fBlockUploads_
  
Указывает, разрешены ли в настоящее время загрузки в новое расположение. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ или _bstrNewWebPath_ уже существуют в другом файле в любом кэше. Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки. См. [ilSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле были удалены из кэша во время работы этого метода.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл в настоящее время синхронизируется в Office приложении.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache удаляет кэш, связанный с SuppliedID, который был предоставлен в Initialize. Это включает всю информацию о файлах, но оставляет файлы как на клиенте, так и на сервере. Этот метод также оставляет объект в частично ненициализованном состоянии. Единственными допустимыми вызовами после этого являются [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Этот метод может вызываться, если Initialize не удается и возвращает E_LSC_CACHEMISMATCH, и удаляет кэш, связанный с SuppliedID, который был предоставлен с ошибкой вызова.
  
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

ServerFileChange сообщает объекту CsiSyncClient COM пометить указанный файл для скачивания. Если файл открыт в приложении Office для редактирования, этот метод возвращается S_OK без маркировки файла для скачивания (приложение уже должно сделать этот шаг, если есть изменения).
  
Этот метод позволит скачивать, если он был отмечен как заблокированные ранее загрузки (см. в нем RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

|Параметр|Описание|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Строка, идентифицируемая с файлом клиента. Это значение должно быть непустым локальным путем с максимальным значением 256 символов. Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове инициализации.  <br/> |
|bstrResourceID  <br/> |Строка, определяемая ResourceID файла. Это значение должно быть непустым с максимальным значением 128 символов.  <br/> |
|bstrWebPath  <br/> |Строка, идентифицирует файл на сервере. Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .  <br/> |
   
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Невозможность установить состояние подключения кэша.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указанный.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Заданное расширение файла не поддерживается объектом CsiSyncClient COM. См. в рублях GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в середине операции.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный  _bstrResourceID,_ отличается от указанного файла FileSystemPath.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже имеет ожидающих изменений в другом кэше и пока не может быть связан с кэшом потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Предоставляемый ВебПат попадает под другой кэш.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Задает кэш в состояние online или автономное. В автономном режиме Office не будет пытаться связываться с сервером для любых файлов в этом кэше, независимо от параметра _fBlockUploads_ каждого отдельного файла. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameters

 _fIsOnline_
  
A boolean determining the connectivity state of the cache. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Невозможность установить состояние подключения кэша.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission используется для переопределения или восстановления синхронизации heuristicsOffice для затрат сети и использования электроэнергии. При работе с 3G или другой дорогостояной сетью или при работе с аккумулятором в сравнении с подключением Office может заблокировать сетевой трафик до более подходящих периодов времени. Потребитель этого API может использовать его для переопределения Office и принудительной синхронизации.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Флаг, который определяет, какие затраты переопределять. См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)
  
 _fEnableSync_
  
Указывает, следует ли принудить к синхронизации, переопределив таким образом эту стоимость, или больше не переопределять ее. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Невыполнение переопределения синхронизации с юристией.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Выгружает кэш из объекта COM и выполняет операции закрытия. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Необходимо вызволить объект COM перед уничтожением. После призыва никакие другие API не могут быть вызваны, объект COM должен быть уничтожен и создан новый, если вы хотите продолжить операции. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Неунинициализация.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Интерфейс IEnumLSCEvent

Этот интерфейс представляет список событий ILSCEvent.
  
**Функции общедоступных членов**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Извлекает следующее событие из списка событий.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameters

 _ppiLSCEvent_
  
Указатель на интерфейс ILSCEvent.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Больше нет событий.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Сбрасывает переустановку в первое событие.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent"></a>Интерфейс ILSCEvent

Этот интерфейс представляет событие синхронизации. Вся информация о событии может быть извлечена из интерфейса.
  
**Функции общедоступных членов**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Обратите внимание, что это значение заполняется при назвав [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) а не в момент создания события, поэтому при смене состояния конфликта у вас будет только текущий статус файла, а не состояние файла. 
  
Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameters

 _pfIsInConflict_
  
Текущее состояние конфликта файла, связанного с событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameters

 _pnError_
  
Ошибка, связанная с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameters

 _pbstrETag_
  
ETag, связанный с этим событием
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Получает тип для этого события.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameters

 _pnEventType_
  
Тип события этого события. Для действительных значений см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Получает локальный рабочий путь для этого события.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameters

 _pbstrLocalWorkingPath_
  
Локальный путь файла, к которому относится это событие. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Получает ИД ресурса для события.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceID_
  
ResourceID файла, связанного с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. При вызове [в ILSCLocalSyncClient::LocalFileChange, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange) [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFi Office le](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) создается это событие. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceIDAttempted_
  
ResourceID, из-за чего произошло это событие. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameters

 _pnSyncErrorType_
  
Тип ошибки, связанный с этим событием. Потенциальные значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недействительными.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameters

 _pbstrWebPath_
  
Указывает веб-путь, связанный с этим событием. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent2"></a>Интерфейс ILSCEvent2

Этот интерфейс содержит дополнительные сведения о событии синхронизации.
  
**Функции общедоступных членов**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Получает сведения о цепочке ошибок о событии синхронизации.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameters

 _pbstrErrorChain_
  
Строка для удержания сведений о цепочке ошибок. Не должно быть null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_NOTIMPL  <br/> |Установленная версия Office не поддерживает этот интерфейс  <br/> |
|E_INVALIDARG  <br/> |Одно или несколько значений параметров являются недействительными.  <br/> |
|E_FAIL  <br/> |Сведения о цепочке ошибок недоступны.  <br/> |
|S_OK  <br/> |Вызов был успешным.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Интерфейс IPartnerActivityCallback

Этот интерфейс предоставляет функцию вызова для объекта CSISyncClient COM.
  
**Функции общедоступных членов**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Это функция вызова на объекте, предоставленном объекту CsiSyncClient COM. Ожидается, что при событии (см. [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) объект CsiSyncClient COM будет вызывать этот метод, сигнализая потребителю. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameters

 _eEventTypeOccurred_
  
Тип события этого события. Дополнительные значения см. в [enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK.
  
## <a name="enumerations"></a>Перечисления

CSISyncClient использует следующие переумерия.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

В этом переумехе указаны категории ошибок, которые могут возникать при синхронизации файла.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Ошибка синхронизации этого события была неожиданной и может потребовать особого рассмотрения. По умолчанию пользователю может потребоваться вмешательство.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Ошибка синхронизации этого события не требует особого внимания. Office будет обрабатываться автоматически.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Ошибка синхронизации этого события требует от пользователя его устранения. Например, ошибка слияния конфликтов требует, чтобы пользователь открыл документ и слил его.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Ошибка синхронизации этого события требует вмешательства пользователя, но не требует особого рассмотрения пользователем.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Ошибка синхронизации этого события требует от потребителя вмешательства в качестве особого случая.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

В этом переумехе указывается тип событий, которые могут произойти для конкретного файла.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Изменения были внесены в локальный файл.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Пользователь открыл файл.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Законченная загрузка файлов изменяется с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Законченная загрузка изменений файла на сервер.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Изменилось состояние конфликта слияния файла.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Добавлен файл.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Файл был удален.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Для файлов пользователя включена синхронизация.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Начался скачивание изменений файла с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Начался процесс загрузки изменений файла на сервер.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Это событие создается при вызове [в ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает столкновение веб-пути или локального пути с другим файлом в кэше Office файла.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

В этом переумехе указывается тип событий, которые могут произойти. Потребителю необходимо вызвать определенные функции ILSCLocalSyncClient в зависимости от типа события.
  
|Enumerator|Описание|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Произошел ilSCEvent. Чтобы получить данные, потребитель должен вызвать [ILSCLocalSyncClient::GetChanges.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Изменены поддерживаемые расширения файлов. Чтобы получить новый список поддерживаемых расширений, потребитель должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

В этом переумечении указаны флаги, используемые для использования в сети. 

|Enumerator|Описание|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True, если переопределена стоимость для дорогих сетей (например, 3G).  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True, если переопределена стоимость использования электроэнергии (например, аккумулятора).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Это переумежение используется для представления состояния синхронизации файла. 
  
|Enumerator|Описание|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True, если в файл сервера отправляются отложенные данные.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True, если есть ожидаемые данные для скачивания из файла сервера.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True, если Office на файле в кэше — это самая недавняя копия данных на диске.  <br/> |
   

