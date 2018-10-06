---
title: Константы MAPI
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Определения констант, объявления интерфейсов MAPI, идентификаторы классов и интерфейсов, используемые API-интерфейсами MAPI.
ms.openlocfilehash: dfc7d16cdb2f57d3f095ceea5fa1ba2eba2e3afe
ms.sourcegitcommit: b91294da1627f6580f52fd3867e2fec8073c6531
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2018
ms.locfileid: "25362045"
---
# <a name="mapi-constants"></a>Константы MAPI

**Область применения**: Outlook 2013 | Outlook 2016 
  
Эта статья содержит определения констант, объявления интерфейсов MAPI, идентификаторы классов и интерфейсов, используемые API-интерфейсами MAPI.
  
## <a name="class-and-interface-identifiers"></a>Идентификаторы классов и интерфейсов

Связывайте символьные имена глобальных уникальных идентификаторов (GUID) с их значениями с помощью макроса DEFINE_GUID, заданного в файле заголовка guiddef.h пакета средств разработки программного обеспечения (SDK) Microsoft Windows, если не указано иное.
  
## <a name="attachment-security-conversion-api"></a>API преобразования безопасности вложений

Этот раздел содержит определения констант и идентификаторы интерфейсов для API безопасности вложений.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Используйте макрос MAPIMETHOD, заданный в файле заголовка mapidefs.h пакета Windows SDK, чтобы определить истинную виртуальную функцию **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Используйте макрос DECLARE_MAPI_INTERFACE_, заданный в файле заголовка mapidefs.h пакета Windows SDK, чтобы определить таблицу виртуальных методов для интерфейса **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>API преобразования MAPI-MIME

Этот раздел содержит определения констант, а также идентификаторы классов и интерфейсов для API преобразования MAPI-MIME.
  
### <a name="constants"></a>Константы

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Определено в файле заголовка winerror.h пакета Microsoft Windows SDK*  <br/> |
   
### <a name="class-identifiers"></a>Идентификаторы классов

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Идентификаторы интерфейсов

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>API автономного состояния

Этот раздел содержит определения констант, а также идентификаторы классов и интерфейсов для API автономного состояния.
  
### <a name="constants"></a>Константы

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Определено в файле заголовка winerror.h пакета Microsoft Windows SDK*  <br/> |
|E_NOINTERFACE  <br/> | *Определено в файле заголовка winerror.h пакета Windows SDK*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**В сети или автономном режиме** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Идентификаторы классов

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Идентификаторы интерфейсов

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a>Именованные свойства Outlook

Этот раздел содержит определения констант для именованных свойств и их пространств имен, а также другие связанные константы.
  
### <a name="definitions-for-named-properties"></a>Определения для именованных свойств

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a>Определения для пространств имен

Указанные ниже глобальные уникальные идентификаторы (GUID) представляют пространства имен для именованных свойств.
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

Определения PSETID см. в разделе "Хранилище MAPI".
  
### <a name="other-constants"></a>Другие константы

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Определено в файле заголовка mapidefs.h.*  <br/> |
|MNID_STRING  <br/> | *Определено в файле заголовка mapidefs.h.*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>API репликации

Этот раздел содержит определения констант, объявления интерфейсов MAPI, идентификаторы классов и интерфейсов для API репликации.
  
### <a name="constants"></a>Константы

Структура [MAPIUID](mapiuid.md), определяющая поставщика службы MAPI: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0x00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0x00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0x00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
### <a name="interface-declarations"></a>Декларации интерфейсов

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Идентификаторы интерфейсов

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

Используйте два следующих идентификатора интерфейса с методом [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md), чтобы открыть и пропустить любую проверку поставщика для объекта папки или объекта сообщения соответственно. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>Хранилище MAPI

Этот раздел содержит определения констант и идентификаторы интерфейсов, которые используются API, взаимодействующими с хранилищем MAPI.
  
### <a name="constants"></a>Константы

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0x00010000)  <br/> |Поставщик хранилища может указать **fnevIndexing** в элементе **ulEventType** структуры **[NOTIFICATION](notification.md)**, чтобы уведомлять индексатора о готовности объекта для индексации. Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.  <br/> |
|FS_NONE  <br/> |0x00  <br/> |Клиент может вызвать **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** и проверить возвращенную битовую маску. Параметр **FS_NONE** указывает, что папка не поддерживает общий доступ.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Клиент может вызвать **IFolderSupport::GetSupportMask** и проверить возвращенную битовую маску. Параметр **FS_SUPPORTS_SHARING** указывает, что папка поддерживает общий доступ.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0x00000001)  <br/> |Определяет процесс отправки индексатору уведомления о готовности объекта для индексации.  <br/> |
|MNID_ID  <br/> |Определено в файле заголовка mapidefs.h пакета Microsoft Windows SDK  <br/> |Значение для поля **ulKind** структуры **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MNID_STRING  <br/> |Определено в файле заголовка mapidefs.h пакета Microsoft Windows SDK.  <br/> |Значение для поля **ulKind** структуры **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0x00000001)  <br/> |Когда клиент задает **MSCAP_SEL_RESTRICTION** в *mscapSelector* для **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, метод **GetCapabilities** может вернуть это значение, если хранилище игнорирует недопустимые параметры в ограничении.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0x00000020)  <br/> |Когда клиент задает **MSCAP_SEL_FOLDER** в *mscapSelector* для **IMSCapabilities::GetCapabilities**, метод **GetCapabilities** может вернуть это значение, если не используется хранилище по умолчанию, поддерживающее домашние страницы папок.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0X00800000)  <br/> |Клиент может использовать свойство **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** для определения характеристики хранилища сообщений. Установка поставщиком хранилища флага **STORE_PUSHER_OK** в битовой маске означает, что обработчик протокола MAPI не выполняет обход хранилища, и хранилище отвечает за отправку всех изменений в виде уведомлений индексатору для индексации сообщений.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Определения для пространств имен

Указанные ниже глобальные уникальные идентификаторы (GUID) представляют пространства имен для именованных свойств. Они индексируются с помощью обработчика протокола MAPI и предназначаются только для чтения.
  
> [!CAUTION]
> Именованные свойства не должны использоваться для создания или изменения элементов. 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnidid-properties"></a>Свойства MNID_ID
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnidstring-properties"></a>Свойства MNID_STRING
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>Идентификаторы интерфейсов

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Чтобы связать следующее символьное имя GUID с его значением, используйте макрос `DEFINE_OLEGUID`, определенный в файле заголовка guiddef.h пакета Windows SDK. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>Константы адресной книги MAPI

Этот раздел содержит определения констант для адресной книги MAPI.
  
### <a name="constants"></a>Константы

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0x00000001)  <br/> |Корневая папка для объекта адресной книги MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0x00000002)  <br/> |Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0x00000003)  <br/> |Объект-контейнер адресной книги.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0x00000004)  <br/> |Объект пользователя, отправляющего сообщение.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0x00000005)  <br/> |Объект списка рассылки.  <br/> |
   
## <a name="additional-mapi-constants"></a>Дополнительные константы MAPI

Этот раздел содержит определения констант, включая коды ошибок, и идентификаторы интерфейсов, используемые API-интерфейсами MAPI, которые ранее не описывались.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0x00000001)  <br/> |Если клиент вызывает метод [IAddrBook::Details](iaddrbook-details.md), он должен установить флаг **DIALOG_MODAL** в параметре _ulFlags_, чтобы отобразить модальное диалоговое окно со сведениями об определенной записи адресной книги. Константа определена в mapidefs.h.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |В Outlook 2007 упакованные PST-хранилища применяют правила и фильтрацию спама для новых сообщений до уведомления о них клиентов MAPI. Поставщик или клиент, использующий метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения в PST-хранилищах, должен установить флаг **ITEMPROC_FORCE** в параметре _ulFlags_ метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md), чтобы указать PST-хранилищу, что сообщение подпадает под применение правил до уведомления любого прослушивающего клиента о получении нового сообщения. Обратите внимание, что такое применение правил относится только к новым сообщениям, созданным на сервере, не являющимся Microsoft Exchange Server, так как Exchange Server применяет правила для сообщений на сервере. Поэтому поставщик или клиент, создающий сообщение, должен передать этот флаг вместе с **NON_EMS_XP_SAVE**, что указывает на применение сервера, отличного от сервера Exchange.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Клиент может вызвать функцию [MAPILogonEx](mapilogonex.md) с установкой флага **MAPI_BG_SESSION** в параметре _flFlags_ для входа в сеанс и выполнения любых операций в фоновом режиме. Как правило, если клиент собирается выполнять обработку в фоновом потоке или отдельном процессе, чтобы он не мешал потоку переднего плана, следует вызвать функцию [MAPILogonEx](mapilogonex.md) с флагом **MAPI_BG_SESSION**. Примером такого использования является клиентское приложение, например подсистема индексирования, открывающая файл личных папок (PST) для доступа в фоновом режиме.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Клиент может вызвать метод [IAddrBook::OpenEntry](iaddrbook-openentry.md) с установкой флага **MAPI_CACHE_ONLY** в параметре _ulFlags_, чтобы открыть запись адресной книги и выполнять последующий доступ к ней только из кэша. Примером такого использования является клиентское приложение, открывающее глобальный список адресов в режиме кэширования Exchange и получающее доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Это значение можно передать функции MAPISendMail Simple MAPI в параметре _ulFlags_, чтобы задать отображение немодального диалогового окна стандартным почтовым приложением. Если ни этот флаг, ни MAPI_DIALOG (0x00000008) не установлены, никакое диалоговое окно не отображается.  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Если Microsoft Office Outlook находится в режиме кэширования Exchange, и хранилище открыто в режиме кэширования, клиент или поставщик службы могут вызвать [IMsgStore::OpenEntry](imsgstore-openentry.md) с установкой флага **MAPI_NO_CACHE** в параметре _ulFlags_, чтобы открыть элемент или папку в удаленном хранилище. Обратите внимание, что при открытии хранилища сообщений с флагом **MDB_ONLINE** на удаленном сервере вам не потребуется использовать флаг **MAPI_NO_CACHE**.  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |Клиент или поставщик службы может вызвать функцию [OpenIMsgOnIStg](openimsgonistg.md) с установкой флага **MAPI_UNICODE** в параметре _ulFlags_, чтобы создавать MSG-файлы с поддержкой Юникода. Итоговый файл [IMessage: IMAPIProp](imessageimapiprop.md) отображает флаг **STORE_UNICODE_OK** в [каноническом свойстве PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) и поддерживает свойства Юникода. Константа определена в mapidefs.h.  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Если Outlook находится в режиме кэширования Exchange, клиент или поставщик службы может вызвать метод [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с установкой флага **MDB_ONLINE** в параметре _ulFlags_, чтобы переопределить подключение к локальному хранилищу сообщений и открыть хранилище на удаленном сервере. Обратите внимание, что в одном сеансе MAPI невозможно одновременно открыть хранилище Exchange в режиме кэширования и режиме без использования кэша. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |Клиент может вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) с установкой флага **NON_EMS_XP_SAVE** в параметре _ulFlags_, чтобы указать, что сообщение доставлено не с сервера Exchange. Этот флаг следует использовать в сочетании с флагом **ITEMPROC_FORCE** в параметре _ulFlags_,  чтобы указать PST-хранилищу, что сообщение подпадает под применение правил до уведомления любого прослушивающего клиента о получении сообщения. Такое применение правил относится только к новым сообщениям, созданным с помощью метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) на сервере, не являющимся сервером Exchange (поскольку в случае сервера Exchange для сообщения уже применены правила).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Клиент может вызвать [IMAPIProp::SaveChanges](imapiprop-savechanges.md) с установкой флага **SPAMFILTER_ONSAVE** в параметре _ulFlags_, чтобы применить фильтр нежелательной почты для сохраненного сообщения. Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя соответствует протоколу SMTP, а сообщение сохранено в хранилище для файлов личных папок (PST).  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Если этот флаг установлен в [каноническом свойстве PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) упакованного PST-хранилища, это означает, что при поступлении в хранилище нового сообщения правила и фильтрация спама применяются для сообщения отдельно. Затем хранилище вызывает метод [IMAPISupport::Notify](imapisupport-notify.md), задавая передаваемый параметр **fnevNewMail** в структуре [NOTIFICATION](notification.md), с отправкой сведений о новом сообщении прослушивающему клиенту. Впоследствии, когда прослушивающий клиент получает уведомление, к сообщению не применяются правила.  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |Если этот флаг включен в [каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), это значит, что хранилище поддерживает хранилище Юникод. Клиент можно проверить наличие флага, чтобы принять решение о запросе или сохранении сведений Юникода в хранилище.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Определения для архивации элементов в папке

Следующие определения констант — это значения, используемые для задания [канонического свойства PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Определения для отображения удаленных объектов

Следующие определения констант и макросов предназначены для отображения удаленных объектов. Дополнительные сведения см. в статье [Каноническое свойство PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Определения для кодов ошибок адресной книги Exchange и хранилища сообщений

Ниже указаны определения кодов ошибок для адресной книги Exchange и хранилища сообщений с возможностью повторного подключения. Последний вызов отключенного глобального каталога (GC) может привести к ошибке **MAPI_E_END_OF_SESSION**, требующей выполнения повторных попыток. 
  
MAPI Outlook поддерживает повторное подключение к серверу GC без специальной перенастройки, но клиенту могут быть возвращены некоторые другие коды ошибок.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Возвращается, если соединение отключено.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Возвращается, если устарел маркер подключения удаленного вызова процедур (RPC). Если маркер текущей транзакции отличается от маркера подключения, это означает, что выполнено повторное подключение, поэтому возвращается параметр **MAPI_E_RECONNECTED**, который может обрабатываться аналогично параметру **MAPI_E_END_OF_SESSION**. Требуется повторная попытка вызова.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Возвращается при отсутствии подключения. Обычно это означает какое-то происшествие в среде, например сбой сервера или отсутствие возможности подключения. Эта ошибка чаще всего случается при использовании профиля в режиме кэширования и попытке обойти кэш для связи с сервером. Если изначально отсутствовала возможность установки соединения кэша с сервером, он может быть в автономном состоянии, при котором может возникать ошибка **MAPI_E_OFFLINE**.  <br/> |
   
Никакая из предыдущих двух ошибок не возвращается в сценариях, в которых они подходят для применения. В большинстве случаев возвращаются ошибки **MAPI\_E_NETWORK_ERROR** или **MAPI_E_CALL_FAILED**. Ни одна из них не появляется при использовании загрузки [Клиент MAPI Microsoft Exchange Server и объекты данных совместной работы 1.2.1](http://support.microsoft.com/kb/171440). 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Определения для квот режима кэширования почтовых ящиков Exchange Server

Следующие определения констант используются в Microsoft Outlook 2010 и Microsoft Outlook 2013, чтобы задавать квоты профиля в режиме кэширования Exchange, аналогичные квотам почтового ящика Exchange, которые в противном случае доступны только для профиля в сети.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Эти свойства сопоставляются с соответствующими сетевыми свойствами и содержат такие же значения в килобайтах. PR_QUOTA_WARNING сопоставляется с PR_STORAGE_QUOTA_LIMIT PR_QUOTA_SEND с PR_QUOTA_PROHIBIT_SEND_QUOTA и PR_QUOTA_RECEIVE с PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Определения для формата сообщения

Следующие определения констант — это значения, которые используются для задания [канонического свойства PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Определения для использования протокола RPC через HTTP

Определения констант, используемые в качестве флагов для задания свойства, см. в разделе [Каноническое свойство PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md). 
  
Определения констант, используемые для задания свойства, см. в разделе [Каноническое свойство PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md). 
  
### <a name="identifiers"></a>Идентификаторы

Связывайте следующие символьные имена GUID с их значениями с помощью макроса `DEFINE_OLEGUID`, заданного в файле заголовка guiddef.h пакета средств разработки программного обеспечения (SDK) Microsoft Windows. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

Следующий идентификатор предназначен для раздела профиля Capone адресной книги, который для поддержки нескольких почтовых ящиков Exchange ([MultiEx](using-multiple-exchange-accounts.md)) содержит свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md), эффективно отключающее контейнер по умолчанию, заданный с помощью [SetDefaultDir](iaddrbook-setdefaultdir.md).
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Идентификаторы интерфейсов

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>Идентификаторы интерфейсов обработчика переопределения PST-файлов

#### <a name="iidipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Сведения об именованных свойствах, используемых в Outlook](about-named-properties-used-by-outlook.md)
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

