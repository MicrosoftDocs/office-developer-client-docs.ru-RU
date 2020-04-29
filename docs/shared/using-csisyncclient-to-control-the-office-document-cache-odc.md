---
title: Использование Ксисинкклиент для управления кэшем документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать Ксисинкклиент для управления кэшем документов Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Использование Ксисинкклиент для управления кэшем документов Office (ODC)

Узнайте, как использовать Ксисинкклиент для управления кэшем документов Office (ODC).
  
Ксисинкклиент — это встроенный COM-сервер (Ксисинкклиент. exe), позволяющий Microsoft OneDrive управлять поведением кэша документов Office (ODC). Например, OneDrive может позвонить на ODC через Ксисинкклиент для отправки и загрузки файлов в конечные точки с включенной поддержкой MS-FSSHTTP. Это позволяет расширенным функциям, поддерживающим обслуживание, в Office, например, совместном редактировании и переходе из автономного режима в оперативный.
  
Ксисинкклиент доступен на рабочем столе Office (x86 и x64). Примечание. в то время как новые версии Office могут поставляться с Ксисинкклиент, этот процесс будет использоваться только для обратной совместимости. Интерфейс Ксисинкклиент и методология управления ODC будут изменены в следующих версиях Office.
  
В настоящее время идентификатор класса имеет значение "ответить только на OneDrive".
  
COM-объект можно использовать в качестве внепроцессных COM-серверов и работает в Ксисинкклиент. exe. В связи с ограничениями на доступ (используемая в ODC), она поставляется с типом бита, в котором находится Office, поэтому платформа x64 Office означает, что используется COM-объект на 64-разрядной версии, или x86 — COM-объект x86. Чтобы обойти это ограничение, при указании CLSCTX_LOCAL_SERVER в составе компонента CoCreateInstance будет размещен COM-объект как внешний COM-сервер, что обеспечивает совместимость с несколькими разрядами.
  
## <a name="interfaces"></a>Интерфейсы

В Ксисинкклиент используются следующие интерфейсы.
  
### <a name="interface-ilsclocalsyncclient"></a>Интерфейс Илсклокалсинкклиент

Это основной интерфейс, используемый для синхронизации файлов в Office.
  
- ProgID: Office. Локалсинкклиент
- CLSID: {14286318 – B6CF — 49a1 — 81FC. D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Предоставляемый COM-объект используется в качестве сервера вне процесса. Указание CLSCTX_LOCAL_SERVER в составе компонента CoCreateInstance обеспечивает возможность совместимости между 64 64 и 32 – 32 процессами.
  
После создания объекта COM необходимо вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) First. После [илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) успешно завершена, вы можете вызвать любой API так часто, как вы хотите и в любом порядке. Вы также можете вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) для уже инициализированного объекта, но при этом ничего не происходит. 
  
Исключениями из предыдущего абзаца являются [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). После вызова [илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) для объекта COM необходимо удалить этот объект и создать новый. [Илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удалит ваш подкэш, удалите все связанные сведения о файле в кэше, но оставьте документы на диске. Кроме того, он оставляет состояние неизменным для связи с кэшем. Это позволяет вызывать [илсклокалсинкклиент:: инициализировать](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать новый кэш без необходимости уничтожения и повторного создания com-объекта. 
  
**Открытые функции элементов**

#### <a name="ilsclocalsyncclientdeletefile"></a>Илсклокалсинкклиент::D Елетефиле

DeleteFile используется для удаления сведений о файле из кэша. Тем не менее, этот метод оставляет связанный файл на диске и на сервере.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _бстрресаурцеид_
  
Строка, которая определяет значение ResourceID файла. Это значение не должно быть пустым (не должно превышать 128 символов). 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Данный ResourceID не находится в кэше.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Инициализация не была успешно вызвана в прошлое.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Файл в настоящее время синхронизируется или открывается, и его невозможно удалить.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>Илсклокалсинкклиент:: Changes
<a name="ILSCLocalSyncClient_GetChanges"> </a>

Метод GetNext возвращает перечислитель объектов Илсцевент, а также возвращает маркер, который передается следующему вызову метода GetNext, предполагая, что потребитель обработал предыдущий набор событий. События, предшествующие указанному _нпревиаусчанжестокен_ , будут удалены и недоступны. Если события для обработки отсутствуют, _пнкуррентчанжестокен_ должно иметь то же значение, что и _Нпревиаусчанжестокен_, но _ппиевентс_ по-прежнему будет задано. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Параметры

 _нпревиаусчанжестокен_
  
Определяет, какое событие было последний раз обработано потребителем. 
  
 _пнкуррентчанжестокен_
  
Определяет Последнее событие, переданное потребителю. Значение не должно быть равно null.
  
 _ппиевентс_
  
Перечислитель для событий, которые передаются потребителю. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>Илсклокалсинкклиент:: Жетклиентнетворксинкпермиссион

Жетклиентнетворксинкпермиссион используется, чтобы запросить, переопределяются ли эвристика синхронизации Office для стоимости сети и энергопотребления. При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Параметры

 _нсптипе_
  
Флаг, определяющий, какой эвристический объект затрат необходимо запросить. В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _пфсинценаблед_
  
Указывает, является ли запрошенный эвристический алгоритм затрат в данный момент перегруженным или нет. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>Илсклокалсинкклиент:: Жетфилестатус

Жетфилестатус используется для сбора сведений о конкретном файле: независимо от того, существует ли он в кэше, если у него есть ожидающая связь с копией на сервере, и если Office 2013 имеет самые актуальные данные из локальной копии. Для определения сведений, к которым необходимо запросить COM-объект Ксисинкклиент, требуется битовый флаг значений [перечисления лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) . 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Параметры

 _бстрресаурцеид_
  
Строка, которая определяет файл на клиенте. Это значение не должно быть пустым, не более 128 символов. 
  
 _сфрекуестедстатус_
  
Флаг, определяющий возвращаемую информацию. В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _пбстрфилесистемпас_
  
Строка, которая определяет расположение файла, определенного _бстрресаурцеид_ в клиенте. Значение не должно быть равно null. 
  
 _пбстретаг_
  
Строка, которая будет содержать тег eTag для файла, указанного с помощью _бстрресаурцеид_. Значение не должно быть равно null. 
  
 _псффилестатус_
  
Флаг, который будет содержать состояние, запрошенное через _сфрекуестедстатус_ , для файла, определенного _бстрресаурцеид_. Значение не должно быть равно null. В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Сведения о файле, указанные в _бстрресаурцеид_ , не существуют в кэше.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Запрошен LSCStatusFlag_LocalFileUnchanged или файл, указанный с помощью _бстрресаурцеид_ , заблокирован или отсутствует.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>Илсклокалсинкклиент:: Жетсуппортедфиликстенсионс
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

Жетсуппортедфиликстенсионс возвращает список расширений файлов с разделением каналов, которые в настоящее время поддерживаются объектом COM Ксисинкклиент. Обратите внимание, что этот список может измениться, а потребитель будет уведомлен об изменении с помощью объекта Ипартнерактивитикаллбакк, предоставленного в [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (см евентоккуред). 
  
Ниже приведен пример возвращаемой строки: "| docx | DOCM | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Параметры

 _пбстрсуппортедфиликстенсионс_
  
Строка, для которой задается набор расширений файлов с разделителем каналов, поддерживаемый COM-объектом Ксисинкклиент. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>Илсклокалсинкклиент:: Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Инициализация должна быть первым вызываемым методом. В противном случае все остальные API будут возвращать E_LSC_NOTINITIALIZED. При вызове метода Initialize для уже инициализированного объекта возвращается S_OK и ничего не происходит. Если возвращается E_LSC_CACHEMISMATCH, вызывающий может вызвать [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) , чтобы удалить кэш, связанный с заданным супплиедид. Тем не менее, в этом случае другие API будут возвращать E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Параметры

 _бстрсупплиедид_
  
Идентифицирует объекта-получателя и используемого кэша. Значение не должно быть пустым (не должно превышать 32 символов). 
  
 _бстрпрогид_
  
Определяет COM-объект потребителя для двусторонней связи. Значение не должно быть пустым (не должно превышать 39 символов). Для получения дополнительных сведений об идентификаторах ProgID см. [ \<\> ](https://docs.microsoft.com/windows/desktop/com/-progid--key) 
  
 _бстрфилесистемдиректорихинт_
  
Определяет корневой каталог, в котором будут храниться локальные файлы. Значение не должно быть пустым (не должно превышать 256 символов). Каталог должен уже существовать. 
  
 _певенткаллбакк_
  
Интерфейс обратного вызова, который Ксисинкклиент будет уведомлять об изменениях. См. Ипартнерактивитикаллбакк:: Евентоккурред. Это значение не должно быть равно null. 
  
 _пфкреатедневкаче_
  
Возвращает значение, указывающее, был ли создан новый кэш. Если с Супплиедид не связан ни один кэш, будет создан один из них. Это значение не должно быть равно null.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Супплиедид уже имеет связанный с ним кэш, но имеет другой ProgId или Филесистемдиректорихинт, чем предоставленные.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Филесистемдиректорихинт (или вложенная папка) уже существует в другом кэше.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |ProgID уже существует в другом кэше.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>Илсклокалсинкклиент:: Локалфилечанже
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

Локалфилечанже используется, чтобы сообщить COM-объекту Ксисинкклиент попытаться отправить указанный файл. Метод подготовит файл для отправки, включая чтение текущего содержимого файла. Если отправка уже ожидается, Предыдущая отправка будет отменена и новое содержимое подготовлено к отправке. Если файл открыт для редактирования в приложении, этот метод возвратит S_OK, не подготавливая файл для отправки (при наличии изменений приложение должно выполнить это действие).
  
Этот метод позволяет отправлять отправку, если он был помечен как отправленные ранее (см. [илсклокалсинкклиент:: ренамефиле ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

 _бстрфилесистемпас_
  
Строка, которая определяет файл на клиенте. Это значение должно быть непустым локальным путем длиной не более 256 символов. Этот путь должен находиться в дереве каталогов, указанном параметром Филесистемдиректорихинт при вызове [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . 
  
 _бстрресаурцеид_
  
Строка, определяющая значение ResourceID файла. Это значение не должно быть пустым (не должно превышать 128 символов). 
  
 _бстрвебпас_
  
Строка, которая определяет файл на сервере. Это значение должно быть непустым, допустимым URL-адресом, но не более чем INTERNET_MAX_URL_LENGTH, https://support.microsoft.com/kb/208427как определено. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного. При возвращении этой ошибки отправляется событие типа LSCEventType_OnFilePathConflict. См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален средней операцией.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Объект COM Ксисинкклиент не поддерживает заданное расширение файла. См. [илсклокалсинкклиент:: жетсуппортедфиликстенсионс ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |COM-объект не запланировать отправку, так как файл в кэше содержал последние изменения с диска.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Файл, указанный в параметре _бстрфилесистемпас_ , отсутствует или заблокирован.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Указанный путь находится в другом кэше.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>Илсклокалсинкклиент:: Ренамефиле
<a name="ILSCLocalSyncClient_RenameFile"> </a>

Ренамефиле будет связывать новый URL-адрес и локальный путь для данного ResourceID. Если файл, указанный с помощью ResourceID, еще не существует в кэше, будет выполнена попытка создать его и пометить для скачивания.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Параметры

 _бстрресаурцеид_
  
Строка, определяющая значение ResourceID файла. Это значение не должно быть пустым (не должно превышать 128 символов). 
  
 _бстрневфилесистемпас_
  
Строка, указывающая новый локальный путь к файлу. Это значение должно быть непустым локальным путем длиной не более 256 символов. Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize. 
  
 _бстрневвебпас_
  
Строка, указывающая новый URL-адрес файла. Это значение должно быть непустым допустимым URL-адресом, но не превышать INTERNET_MAX_URL_LENGTH, как https://support.microsoft.com/kb/208427определено. 
  
 _фблоккуплоадс_
  
Указывает, разрешена ли в данный момент отправка в новое расположение. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_Бстрневфилесистемпас_ или _бстрневвебпас_ уже существуют в другом файле в любом кэше. При возвращении этой ошибки отправляется событие типа LSCEventType_OnFilePathConflict. См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |При выполнении этого метода сведения о файле были удалены из кэша.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |В настоящий момент указанный файл синхронизируется в приложении Office.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>Илсклокалсинкклиент:: Ресеткаче
<a name="ILSCLocalSyncClient_ResetCache"> </a>

Ресеткаче удалит кэш, связанный с Супплиедид, который был предоставлен при инициализации. Сюда входят все сведения о файле, но файлы будут оставлены как на клиенте, так и на сервере. Этот метод также оставляет объект в частично неинициализированном состоянии. Единственные допустимые вызовы после этого [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Этот метод можно вызвать, если происходит сбой инициализации и возвращается E_LSC_CACHEMISMATCH, и удаляется кэш, связанный с Супплиедид, который был предоставлен при сбое вызова.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Параметры

Нет
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Вызов завершился ошибкой.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>Илсклокалсинкклиент:: Серверфилечанже
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Серверфилечанже указывает COM-объекту Ксисинкклиент пометить указанный файл для загрузки. Если файл открыт в приложении Office для редактирования, этот метод возвратит S_OK, не помечая файл для загрузки (при наличии изменений приложение должно выполнить это действие).
  
Этот метод позволит загружать загружаемые файлы, если он был помечен как загруженные ранее (см. Ренамефиле).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Параметры

|Параметр|Описание|
|:-----|:-----|
|бстрфилесистемпас  <br/> |Строка, которая определяет файл на клиенте. Это значение должно быть непустым локальным путем длиной не более 256 символов. Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize.  <br/> |
|бстрресаурцеид  <br/> |Строка, определяющая значение ResourceID файла. Это значение не должно быть пустым (не должно превышать 128 символов).  <br/> |
|бстрвебпас  <br/> |Строка, которая определяет файл на сервере. Это значение должно быть непустым допустимым URL-адресом, но не превышать INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Не удалось задать состояние подключения кэша.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Объект COM Ксисинкклиент не поддерживает заданное расширение файла. Обратитесь к разделу Жетсуппортедфиликстенсионс.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Файл был удален в средней операции.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Указанный путь находится в другом кэше.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>Илсклокалсинкклиент:: Сетклиентконнективитистате
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Переводит кэш в оперативный или автономный режим. В автономном режиме Office не будет пытаться установить соединение с сервером для всех файлов в этом кэше, независимо от параметра _фблоккуплоадс_ каждого отдельного файла. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Параметры

 _фисонлине_
  
Логическое значение, определяющее состояние подключения кэша. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Не удалось задать состояние подключения кэша.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>Илсклокалсинкклиент:: Сетклиентнетворксинкпермиссион
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Сетклиентнетворксинкпермиссион используется для переопределения или Рестореоффице эвристических правил синхронизации для стоимости сети и потребления электроэнергии. При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время. Потребитель этого API может использовать его для переопределения эвристики Office и принудительной синхронизации.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Параметры

 _нсптипе_
  
Флаг, определяющий, какой эвристикой затрат следует переопределить. В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _фенаблесинк_
  
Указывает, следует ли принудительно выполнять синхронизацию, таким образом переопределяя более эвристику затрат или более не переопределять ее. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Не удалось переопределить эвристику синхронизации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>Илсклокалсинкклиент:: Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Выгрузка кэша из COM-объекта и выполнение операций закрытия. [Илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Перед удалением COM-объекта необходимо вызвать метод. После вызова другие API не могут вызываться, COM-объект должен быть удален, а новый — создан, если вы хотите продолжить операции. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Сбой при невозможности инициализации.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.  <br/> |
|S_OK  <br/> |The call succeeded.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Интерфейс Иенумлсцевент

Этот интерфейс представляет список событий Илсцевент.
  
**Открытые функции элементов**

#### <a name="ienumlsceventfnext"></a>Иенумлсцевент:: Фнекст

Извлекает следующее событие из списка событий.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Параметры

 _ппилсцевент_
  
Указатель на интерфейс Илсцевент.
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_FAIL  <br/> |Больше нет событий.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ienumlsceventreset"></a>Иенумлсцевент:: Reset

Сбрасывает перечислитель к первому событию.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Параметры

Нет.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent"></a>Интерфейс Илсцевент

Этот интерфейс представляет событие синхронизации. Все сведения о событии можно получить из интерфейса.
  
**Открытые функции элементов**

#### <a name="ilsceventgetconflictstatus"></a>Илсцевент:: Жетконфликтстатус

Обратите внимание на то, что это значение заполняется при вызове метода [илсклокалсинкклиент::-Changes](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) , а не при создании события, поэтому отображается только текущее состояние файла, а не его состояние при изменении состояния конфликта. 
  
Это значение заполняется только при LSCEventType_OnLocalConflictStateChanged [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Параметры

 _пфисинконфликт_
  
Текущее состояние конфликта файла, связанного с событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeterror"></a>Илсцевент:: ошибка

Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Параметры

 _пнеррор_
  
Ошибка, связанная с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetetag"></a>Илсцевент::/ETag

Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Параметры

 _пбстретаг_
  
ETag, связанный с этим событием
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>Илсцевент:: Жетевенттипе

Получает тип данного события.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Параметры

 _пневенттипе_
  
Тип события для этого события. Допустимые значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) . Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>Илсцевент:: Жетлокалворкингпас

Получает путь к локальному рабочему пути для этого события.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Параметры

 _пбстрлокалворкингпас_
  
Локальный путь к файлу, к которому относится данное событие. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>Илсцевент:: Жетресаурцеид

Получает идентификатор ресурса для события.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Параметры

 _пбстрресаурцеид_
  
ResourceID файла, связанного с этим событием.
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>Илсцевент:: Жетресаурцеидаттемптед

Это значение заполняется только при LSCEventType_OnFilePathConflict [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события. При вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) это приведет к созданию веб-пути или конфликта локального пути с другим файлом в кэше файлов Office. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Параметры

 _пбстрресаурцеидаттемптед_
  
Значение ResourceID, которое вызвало создание события. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>Илсцевент:: Жетсинцеррортипе

Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Параметры

 _пнсинцеррортипе_
  
Тип ошибки, связанный с этим событием. Возможные значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) . Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_INVALIDARG  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>Илсцевент:: Жетвебпас

Это значение заполняется только при LSCEventType_OnFilePathConflict [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Параметры

 _пбстрвебпас_
  
Указывает веб-путь, связанный с этим событием. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK. 
  
### <a name="interface-ilscevent2"></a>Интерфейс ILSCEvent2

Этот интерфейс содержит дополнительные сведения о событии синхронизации.
  
**Открытые функции элементов**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2:: Жетеррорчаин

Получает сведения о цепочке ошибок для события синхронизации.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Параметры

 _пбстреррорчаин_
  
Строка, в которой хранятся сведения о цепочке ошибок. Значение не должно быть равно null. 
  
##### <a name="return-values"></a>Возвращаемые значения

|Значение|Описание|
|:-----|:-----|
|E_NOTIMPL  <br/> |Установленная версия Office не поддерживает этот интерфейс  <br/> |
|E_INVALIDARG  <br/> |Одно или несколько значений параметров являются недопустимыми.  <br/> |
|E_FAIL  <br/> |Информация о цепочке ошибок недоступна.  <br/> |
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Интерфейс Ипартнерактивитикаллбакк

Этот интерфейс предоставляет функцию обратного вызова для COM-объекта Ксисинкклиент.
  
**Открытые функции элементов**

#### <a name="ipartneractivitycallbackeventoccurred"></a>Ипартнерактивитикаллбакк:: Евентоккурред

Это функция обратного вызова для объекта, данного COM-объекта Ксисинкклиент. Ожидается, что при возникновении события (см. [перечисление лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) COM-объект ксисинкклиент вызывает этот метод, засигнализациет получателя. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Параметры

 _ивенттипеоккурред_
  
Тип события для этого события. Допустимые значения приведены в разделе [enum лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) . 
  
##### <a name="return-values"></a>Возвращаемые значения

Всегда возвращает S_OK.
  
## <a name="enumerations"></a>Перечисления

В Ксисинкклиент используются следующие перечисления.
  
### <a name="enum-lsceventsyncerrortype"></a>Перечисление Лсцевентсинцеррортипе
<a name="Enum_LSCEventSyncErrorType"> </a>

Это перечисление указывает категории ошибок, которые могут возникать при синхронизации файла.
  
|Перечисляем|Описание|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Ошибка синхронизации этого события, которая может требовать особой важности. По умолчанию пользователю может потребоваться последовать.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Ошибка синхронизации этого события не требует особой важности. Office будет автоматически обрабатывать его.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Для ошибки синхронизации этого события необходимо, чтобы пользователь решил эту проблему. Например, для ошибки слияния необходимо, чтобы пользователь открыл документ, а затем слить его.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Для ошибки синхронизации этого события необходимо, чтобы потребитель натребовался, но не обязательно должен быть особым вопросом.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Для ошибки синхронизации этого события необходимо, чтобы потребитель был особым случаем.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Перечисление Лсцевенттипе
<a name="Enum_LSCEventType"> </a>

Это перечисление определяет тип событий, которые могут возникать в определенном файле.
  
|Перечисляем|Описание|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Изменения, внесенные в локальный файл.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Пользователь открыл файл.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Загрузка изменений файлов с сервера завершена.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Отгрузка изменений файлов на сервер завершена.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Изменено состояние конфликта слияния файла.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Добавлен файл.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Удален файл.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Синхронизация для файлов пользователя включена.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Началась загрузка изменений файлов с сервера.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Начата отправка изменений файлов на сервер.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Это событие создается при вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [Илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает веб-путь или конфликты локального пути с другим файлом в кэше файлов Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Перечисление Лсцевенттипеоккурред
<a name="Enum_LSCEventTypeOccurred"> </a>

Это перечисление определяет тип событий, которые могут возникнуть. Потребитель должен вызывать определенные функции Илсклокалсинкклиент на основе типа события.
  
|Перечисляем|Описание|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Произошла Илсцевент. Потребитель должен вызывать [илсклокалсинкклиент::-Changes](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для получения данных.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Изменены поддерживаемые расширения файлов. Потребитель должен вызвать [илсклокалсинкклиент:: жетсуппортедфиликстенсионс](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) , чтобы получить новый список поддерживаемых расширений.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Перечисление Лскнетворксинкпермиссионтипе
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Это перечисление указывает флаги, используемые для эвристики стоимости сети. 

|Перечисляем|Описание|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |Значение true, если эвристика затрат для дорогостоящих сетей (например, 3G) переопределена.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |Имеет значение true, если переопределяется эвристика затрат для использования питания (например, батарея).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Перечисление Лскстатусфлаг
<a name="Enum_LSCStatusFlag"> </a>

Это перечисление используется для представления состояния синхронизации файла. 
  
|Перечисляем|Описание|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |Значение true, если имеются ожидающие данные для отправки в файл сервера.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |Значение true, если ожидаются данные, которые требуется скачать из файла сервера.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |Значение true, если в кэше данных в файле есть последняя копия данных на диске.  <br/> |
   

