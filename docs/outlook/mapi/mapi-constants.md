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
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393735"
---
# <a name="mapi-constants"></a><span data-ttu-id="21b63-103">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="21b63-103">MAPI Constants</span></span>

<span data-ttu-id="21b63-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21b63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21b63-105">Эта статья содержит определения констант, объявления интерфейсов MAPI, идентификаторы классов и интерфейсов, используемые API-интерфейсами MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="21b63-106">Идентификаторы классов и интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-106">Class and interface identifiers</span></span>

<span data-ttu-id="21b63-107">Связывайте символьные имена глобальных уникальных идентификаторов (GUID) с их значениями с помощью макроса DEFINE_GUID, заданного в файле заголовка guiddef.h пакета средств разработки программного обеспечения (SDK) Microsoft Windows, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="21b63-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="21b63-108">API преобразования безопасности вложений</span><span class="sxs-lookup"><span data-stu-id="21b63-108">Attachment security conversion API</span></span>

<span data-ttu-id="21b63-109">Этот раздел содержит определения констант и идентификаторы интерфейсов для API безопасности вложений.</span><span class="sxs-lookup"><span data-stu-id="21b63-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="21b63-110">Используйте макрос MAPIMETHOD, заданный в файле заголовка mapidefs.h пакета Windows SDK, чтобы определить истинную виртуальную функцию **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="21b63-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="21b63-111">Используйте макрос DECLARE_MAPI_INTERFACE_, заданный в файле заголовка mapidefs.h пакета Windows SDK, чтобы определить таблицу виртуальных методов для интерфейса **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="21b63-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="21b63-112">API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="21b63-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="21b63-113">Этот раздел содержит определения констант, а также идентификаторы классов и интерфейсов для API преобразования MAPI-MIME.</span><span class="sxs-lookup"><span data-stu-id="21b63-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="21b63-114">Константы</span><span class="sxs-lookup"><span data-stu-id="21b63-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21b63-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="21b63-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="21b63-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="21b63-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="21b63-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="21b63-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="21b63-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="21b63-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="21b63-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="21b63-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="21b63-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="21b63-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="21b63-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="21b63-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="21b63-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="21b63-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="21b63-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="21b63-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="21b63-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="21b63-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="21b63-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="21b63-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="21b63-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="21b63-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="21b63-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="21b63-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="21b63-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="21b63-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="21b63-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="21b63-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="21b63-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="21b63-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="21b63-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="21b63-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="21b63-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="21b63-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="21b63-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="21b63-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="21b63-134">*Определено в файле заголовка winerror.h пакета Microsoft Windows SDK*</span><span class="sxs-lookup"><span data-stu-id="21b63-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="21b63-135">Идентификаторы классов</span><span class="sxs-lookup"><span data-stu-id="21b63-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="21b63-136">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="21b63-137">API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="21b63-137">About the Offline State API</span></span>

<span data-ttu-id="21b63-138">Этот раздел содержит определения констант, а также идентификаторы классов и интерфейсов для API автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="21b63-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="21b63-139">Константы</span><span class="sxs-lookup"><span data-stu-id="21b63-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21b63-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="21b63-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="21b63-141">*Определено в файле заголовка winerror.h пакета Microsoft Windows SDK*</span><span class="sxs-lookup"><span data-stu-id="21b63-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="21b63-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="21b63-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="21b63-143">*Определено в файле заголовка winerror.h пакета Windows SDK*</span><span class="sxs-lookup"><span data-stu-id="21b63-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="21b63-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="21b63-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="21b63-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="21b63-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="21b63-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="21b63-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="21b63-147">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="21b63-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="21b63-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="21b63-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="21b63-149">1</span><span class="sxs-lookup"><span data-stu-id="21b63-149">1</span></span>  <br/> |
|<span data-ttu-id="21b63-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="21b63-151">0x1</span><span class="sxs-lookup"><span data-stu-id="21b63-151">0x1</span></span>  <br/> |
|<span data-ttu-id="21b63-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="21b63-153">0x2</span><span class="sxs-lookup"><span data-stu-id="21b63-153">0x2</span></span>  <br/> |
|<span data-ttu-id="21b63-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="21b63-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="21b63-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="21b63-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="21b63-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="21b63-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="21b63-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b63-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="21b63-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="21b63-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="21b63-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="21b63-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="21b63-160">**В сети или автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="21b63-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="21b63-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="21b63-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="21b63-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="21b63-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="21b63-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="21b63-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="21b63-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="21b63-167">Идентификаторы классов</span><span class="sxs-lookup"><span data-stu-id="21b63-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="21b63-168">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="21b63-169">Именованные свойства Outlook</span><span class="sxs-lookup"><span data-stu-id="21b63-169">Outlook named properties</span></span>

<span data-ttu-id="21b63-170">Этот раздел содержит определения констант для именованных свойств и их пространств имен, а также другие связанные константы.</span><span class="sxs-lookup"><span data-stu-id="21b63-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="21b63-171">Определения для именованных свойств</span><span class="sxs-lookup"><span data-stu-id="21b63-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="21b63-172">Определения для пространств имен</span><span class="sxs-lookup"><span data-stu-id="21b63-172">Definitions for namespaces</span></span>

<span data-ttu-id="21b63-173">Указанные ниже глобальные уникальные идентификаторы (GUID) представляют пространства имен для именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="21b63-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="21b63-174">Определения PSETID см. в разделе "Хранилище MAPI".</span><span class="sxs-lookup"><span data-stu-id="21b63-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="21b63-175">Другие константы</span><span class="sxs-lookup"><span data-stu-id="21b63-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21b63-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="21b63-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="21b63-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="21b63-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="21b63-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="21b63-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="21b63-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="21b63-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="21b63-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="21b63-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="21b63-181">*Определено в файле заголовка mapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="21b63-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="21b63-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="21b63-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="21b63-183">*Определено в файле заголовка mapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="21b63-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="21b63-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="21b63-184">mtgNone</span></span>  <br/> |<span data-ttu-id="21b63-185">0x0</span><span class="sxs-lookup"><span data-stu-id="21b63-185">0x0</span></span>  <br/> |
|<span data-ttu-id="21b63-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="21b63-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="21b63-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="21b63-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="21b63-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="21b63-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="21b63-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="21b63-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="21b63-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="21b63-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="21b63-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="21b63-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="21b63-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="21b63-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="21b63-196">API репликации</span><span class="sxs-lookup"><span data-stu-id="21b63-196">About the Replication API</span></span>

<span data-ttu-id="21b63-197">Этот раздел содержит определения констант, объявления интерфейсов MAPI, идентификаторы классов и интерфейсов для API репликации.</span><span class="sxs-lookup"><span data-stu-id="21b63-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="21b63-198">Константы</span><span class="sxs-lookup"><span data-stu-id="21b63-198">Constants</span></span>

<span data-ttu-id="21b63-199">Структура [MAPIUID](mapiuid.md), определяющая поставщика службы MAPI:</span><span class="sxs-lookup"><span data-stu-id="21b63-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="21b63-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="21b63-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="21b63-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="21b63-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="21b63-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="21b63-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="21b63-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="21b63-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="21b63-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b63-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="21b63-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="21b63-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21b63-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="21b63-211">((ULONG) 0x00000800)</span><span class="sxs-lookup"><span data-stu-id="21b63-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="21b63-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="21b63-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="21b63-213">((ULONG) 0x00001000)</span><span class="sxs-lookup"><span data-stu-id="21b63-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="21b63-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="21b63-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="21b63-215">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="21b63-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="21b63-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="21b63-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="21b63-217">0</span><span class="sxs-lookup"><span data-stu-id="21b63-217">0%</span></span>  <br/> |
|<span data-ttu-id="21b63-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="21b63-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="21b63-219">1</span><span class="sxs-lookup"><span data-stu-id="21b63-219">1</span></span>  <br/> |
|<span data-ttu-id="21b63-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="21b63-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="21b63-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="21b63-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="21b63-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="21b63-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="21b63-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="21b63-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="21b63-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="21b63-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="21b63-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="21b63-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="21b63-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="21b63-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="21b63-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="21b63-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="21b63-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="21b63-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="21b63-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="21b63-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="21b63-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="21b63-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="21b63-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="21b63-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="21b63-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="21b63-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="21b63-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="21b63-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="21b63-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="21b63-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="21b63-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="21b63-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="21b63-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="21b63-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="21b63-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="21b63-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="21b63-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="21b63-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="21b63-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="21b63-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="21b63-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="21b63-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="21b63-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="21b63-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="21b63-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="21b63-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="21b63-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="21b63-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="21b63-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="21b63-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="21b63-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="21b63-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="21b63-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="21b63-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="21b63-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="21b63-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="21b63-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="21b63-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="21b63-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="21b63-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="21b63-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="21b63-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="21b63-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="21b63-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="21b63-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="21b63-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="21b63-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="21b63-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="21b63-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="21b63-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="21b63-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b63-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="21b63-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="21b63-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="21b63-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="21b63-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="21b63-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="21b63-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="21b63-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="21b63-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="21b63-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="21b63-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="21b63-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="21b63-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="21b63-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="21b63-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="21b63-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="21b63-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="21b63-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="21b63-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="21b63-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="21b63-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="21b63-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="21b63-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="21b63-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="21b63-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="21b63-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="21b63-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="21b63-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="21b63-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="21b63-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="21b63-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="21b63-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="21b63-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="21b63-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="21b63-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="21b63-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="21b63-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="21b63-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="21b63-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="21b63-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="21b63-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="21b63-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21b63-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="21b63-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="21b63-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="21b63-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="21b63-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="21b63-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="21b63-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="21b63-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="21b63-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="21b63-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="21b63-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="21b63-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="21b63-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="21b63-310">Декларации интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="21b63-311">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-311">Interface identifiers</span></span>

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

<span data-ttu-id="21b63-312">Используйте два следующих идентификатора интерфейса с методом [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md), чтобы открыть и пропустить любую проверку поставщика для объекта папки или объекта сообщения соответственно.</span><span class="sxs-lookup"><span data-stu-id="21b63-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="21b63-313">Хранилище MAPI</span><span class="sxs-lookup"><span data-stu-id="21b63-313">MAPI store</span></span>

<span data-ttu-id="21b63-314">Этот раздел содержит определения констант и идентификаторы интерфейсов, которые используются API, взаимодействующими с хранилищем MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="21b63-315">Константы</span><span class="sxs-lookup"><span data-stu-id="21b63-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="21b63-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="21b63-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="21b63-317">((ULONG) 0x00010000)</span><span class="sxs-lookup"><span data-stu-id="21b63-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="21b63-318">Поставщик хранилища может указать **fnevIndexing** в элементе **ulEventType** структуры **[NOTIFICATION](notification.md)**, чтобы уведомлять индексатора о готовности объекта для индексации.</span><span class="sxs-lookup"><span data-stu-id="21b63-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="21b63-319">Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="21b63-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="21b63-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="21b63-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="21b63-321">0x00</span><span class="sxs-lookup"><span data-stu-id="21b63-321">0x00</span></span>  <br/> |<span data-ttu-id="21b63-322">Клиент может вызвать **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** и проверить возвращенную битовую маску.</span><span class="sxs-lookup"><span data-stu-id="21b63-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="21b63-323">Параметр **FS_NONE** указывает, что папка не поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="21b63-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="21b63-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="21b63-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="21b63-325">0x01</span><span class="sxs-lookup"><span data-stu-id="21b63-325">0x01</span></span>  <br/> |<span data-ttu-id="21b63-326">Клиент может вызвать **IFolderSupport::GetSupportMask** и проверить возвращенную битовую маску.</span><span class="sxs-lookup"><span data-stu-id="21b63-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="21b63-327">Параметр **FS_SUPPORTS_SHARING** указывает, что папка поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="21b63-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="21b63-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="21b63-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="21b63-329">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="21b63-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="21b63-330">Определяет процесс отправки индексатору уведомления о готовности объекта для индексации.</span><span class="sxs-lookup"><span data-stu-id="21b63-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="21b63-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="21b63-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="21b63-332">Определено в файле заголовка mapidefs.h пакета Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="21b63-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="21b63-333">Значение для поля **ulKind** структуры **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="21b63-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="21b63-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="21b63-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="21b63-335">Определено в файле заголовка mapidefs.h пакета Microsoft Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="21b63-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="21b63-336">Значение для поля **ulKind** структуры **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="21b63-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="21b63-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="21b63-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="21b63-338">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="21b63-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="21b63-339">Когда клиент задает **MSCAP_SEL_RESTRICTION** в *mscapSelector* для **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, метод **GetCapabilities** может вернуть это значение, если хранилище игнорирует недопустимые параметры в ограничении.</span><span class="sxs-lookup"><span data-stu-id="21b63-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="21b63-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="21b63-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="21b63-341">((ULONG) 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="21b63-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="21b63-342">Когда клиент задает **MSCAP_SEL_FOLDER** в *mscapSelector* для **IMSCapabilities::GetCapabilities**, метод **GetCapabilities** может вернуть это значение, если не используется хранилище по умолчанию, поддерживающее домашние страницы папок.</span><span class="sxs-lookup"><span data-stu-id="21b63-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="21b63-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="21b63-344">((ULONG) 0X00800000)</span><span class="sxs-lookup"><span data-stu-id="21b63-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="21b63-345">Клиент может использовать свойство **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** для определения характеристики хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="21b63-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="21b63-346">Установка поставщиком хранилища флага **STORE_PUSHER_OK** в битовой маске означает, что обработчик протокола MAPI не выполняет обход хранилища, и хранилище отвечает за отправку всех изменений в виде уведомлений индексатору для индексации сообщений.</span><span class="sxs-lookup"><span data-stu-id="21b63-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="21b63-347">Определения для пространств имен</span><span class="sxs-lookup"><span data-stu-id="21b63-347">Definitions for namespaces</span></span>

<span data-ttu-id="21b63-348">Указанные ниже глобальные уникальные идентификаторы (GUID) представляют пространства имен для именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="21b63-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="21b63-349">Они индексируются с помощью обработчика протокола MAPI и предназначаются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="21b63-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="21b63-350">Именованные свойства не должны использоваться для создания или изменения элементов.</span><span class="sxs-lookup"><span data-stu-id="21b63-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="21b63-351">Свойства MNID_ID</span><span class="sxs-lookup"><span data-stu-id="21b63-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="21b63-352">Свойства MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="21b63-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="21b63-353">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="21b63-354">Чтобы связать следующее символьное имя GUID с его значением, используйте макрос `DEFINE_OLEGUID`, определенный в файле заголовка guiddef.h пакета Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="21b63-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="21b63-355">Константы адресной книги MAPI</span><span class="sxs-lookup"><span data-stu-id="21b63-355">MAPI Address Book</span></span>

<span data-ttu-id="21b63-356">Этот раздел содержит определения констант для адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="21b63-357">Константы</span><span class="sxs-lookup"><span data-stu-id="21b63-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="21b63-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="21b63-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="21b63-359">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="21b63-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="21b63-360">Корневая папка для объекта адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="21b63-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="21b63-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="21b63-362">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="21b63-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="21b63-363">Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="21b63-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="21b63-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="21b63-365">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="21b63-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="21b63-366">Объект-контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="21b63-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="21b63-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="21b63-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="21b63-368">((ULONG) 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="21b63-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="21b63-369">Объект пользователя, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="21b63-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="21b63-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="21b63-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="21b63-371">((ULONG) 0x00000005)</span><span class="sxs-lookup"><span data-stu-id="21b63-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="21b63-372">Объект списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="21b63-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="21b63-373">Дополнительные константы MAPI</span><span class="sxs-lookup"><span data-stu-id="21b63-373">Additional MAPI constants</span></span>

<span data-ttu-id="21b63-374">Этот раздел содержит определения констант, включая коды ошибок, и идентификаторы интерфейсов, используемые API-интерфейсами MAPI, которые ранее не описывались.</span><span class="sxs-lookup"><span data-stu-id="21b63-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="21b63-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="21b63-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="21b63-376">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="21b63-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="21b63-377">Если клиент вызывает метод [IAddrBook::Details](iaddrbook-details.md), он должен установить флаг **DIALOG_MODAL** в параметре _ulFlags_, чтобы отобразить модальное диалоговое окно со сведениями об определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="21b63-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="21b63-378">Константа определена в mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="21b63-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="21b63-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="21b63-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="21b63-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="21b63-380">0x00000800</span></span>  <br/> |<span data-ttu-id="21b63-381">В Outlook 2007 упакованные PST-хранилища применяют правила и фильтрацию спама для новых сообщений до уведомления о них клиентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="21b63-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="21b63-382">Поставщик или клиент, использующий метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения в PST-хранилищах, должен установить флаг **ITEMPROC_FORCE** в параметре _ulFlags_ метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md), чтобы указать PST-хранилищу, что сообщение подпадает под применение правил до уведомления любого прослушивающего клиента о получении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="21b63-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="21b63-383">Обратите внимание, что такое применение правил относится только к новым сообщениям, созданным на сервере, не являющимся Microsoft Exchange Server, так как Exchange Server применяет правила для сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="21b63-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="21b63-384">Поэтому поставщик или клиент, создающий сообщение, должен передать этот флаг вместе с **NON_EMS_XP_SAVE**, что указывает на применение сервера, отличного от сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="21b63-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="21b63-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="21b63-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="21b63-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="21b63-386">0x00200000</span></span>  <br/> |<span data-ttu-id="21b63-387">Клиент может вызвать функцию [MAPILogonEx](mapilogonex.md) с установкой флага **MAPI_BG_SESSION** в параметре _flFlags_ для входа в сеанс и выполнения любых операций в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="21b63-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="21b63-388">Как правило, если клиент собирается выполнять обработку в фоновом потоке или отдельном процессе, чтобы он не мешал потоку переднего плана, следует вызвать функцию [MAPILogonEx](mapilogonex.md) с флагом **MAPI_BG_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="21b63-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="21b63-389">Примером такого использования является клиентское приложение, например подсистема индексирования, открывающая файл личных папок (PST) для доступа в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="21b63-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="21b63-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="21b63-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="21b63-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="21b63-391">0x00004000</span></span>  <br/> |<span data-ttu-id="21b63-392">Клиент может вызвать метод [IAddrBook::OpenEntry](iaddrbook-openentry.md) с установкой флага **MAPI_CACHE_ONLY** в параметре _ulFlags_, чтобы открыть запись адресной книги и выполнять последующий доступ к ней только из кэша.</span><span class="sxs-lookup"><span data-stu-id="21b63-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="21b63-393">Примером такого использования является клиентское приложение, открывающее глобальный список адресов в режиме кэширования Exchange и получающее доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="21b63-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="21b63-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="21b63-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="21b63-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="21b63-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="21b63-396">Это значение можно передать функции MAPISendMail Simple MAPI в параметре _ulFlags_, чтобы задать отображение немодального диалогового окна стандартным почтовым приложением.</span><span class="sxs-lookup"><span data-stu-id="21b63-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="21b63-397">Если ни этот флаг, ни MAPI_DIALOG (0x00000008) не установлены, никакое диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="21b63-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="21b63-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="21b63-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="21b63-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="21b63-399">0x00000200</span></span>  <br/> |<span data-ttu-id="21b63-400">Если Microsoft Office Outlook находится в режиме кэширования Exchange, и хранилище открыто в режиме кэширования, клиент или поставщик службы могут вызвать [IMsgStore::OpenEntry](imsgstore-openentry.md) с установкой флага **MAPI_NO_CACHE** в параметре _ulFlags_, чтобы открыть элемент или папку в удаленном хранилище.</span><span class="sxs-lookup"><span data-stu-id="21b63-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="21b63-401">Обратите внимание, что при открытии хранилища сообщений с флагом **MDB_ONLINE** на удаленном сервере вам не потребуется использовать флаг **MAPI_NO_CACHE**.</span><span class="sxs-lookup"><span data-stu-id="21b63-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="21b63-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21b63-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="21b63-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="21b63-403">0x80000000</span></span>  <br/> |<span data-ttu-id="21b63-404">Клиент или поставщик службы может вызвать функцию [OpenIMsgOnIStg](openimsgonistg.md) с установкой флага **MAPI_UNICODE** в параметре _ulFlags_, чтобы создавать MSG-файлы с поддержкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="21b63-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="21b63-405">Итоговый файл [IMessage: IMAPIProp](imessageimapiprop.md) отображает флаг **STORE_UNICODE_OK** в [каноническом свойстве PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) и поддерживает свойства Юникода.</span><span class="sxs-lookup"><span data-stu-id="21b63-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="21b63-406">Константа определена в mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="21b63-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="21b63-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="21b63-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="21b63-408">0x00000100</span></span>  <br/> |<span data-ttu-id="21b63-409">Если Outlook находится в режиме кэширования Exchange, клиент или поставщик службы может вызвать метод [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с установкой флага **MDB_ONLINE** в параметре _ulFlags_, чтобы переопределить подключение к локальному хранилищу сообщений и открыть хранилище на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="21b63-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="21b63-410">Обратите внимание, что в одном сеансе MAPI невозможно одновременно открыть хранилище Exchange в режиме кэширования и режиме без использования кэша.</span><span class="sxs-lookup"><span data-stu-id="21b63-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="21b63-411">Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.</span><span class="sxs-lookup"><span data-stu-id="21b63-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="21b63-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="21b63-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="21b63-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="21b63-413">0x00001000</span></span>  <br/> |<span data-ttu-id="21b63-414">Клиент может вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) с установкой флага **NON_EMS_XP_SAVE** в параметре _ulFlags_, чтобы указать, что сообщение доставлено не с сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="21b63-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="21b63-415">Этот флаг следует использовать в сочетании с флагом **ITEMPROC_FORCE** в параметре _ulFlags_,  чтобы указать PST-хранилищу, что сообщение подпадает под применение правил до уведомления любого прослушивающего клиента о получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="21b63-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="21b63-416">Такое применение правил относится только к новым сообщениям, созданным с помощью метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) на сервере, не являющимся сервером Exchange (поскольку в случае сервера Exchange для сообщения уже применены правила).</span><span class="sxs-lookup"><span data-stu-id="21b63-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="21b63-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="21b63-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="21b63-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="21b63-418">0x00000080</span></span>  <br/> |<span data-ttu-id="21b63-419">Клиент может вызвать [IMAPIProp::SaveChanges](imapiprop-savechanges.md) с установкой флага **SPAMFILTER_ONSAVE** в параметре _ulFlags_, чтобы применить фильтр нежелательной почты для сохраненного сообщения.</span><span class="sxs-lookup"><span data-stu-id="21b63-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="21b63-420">Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя соответствует протоколу SMTP, а сообщение сохранено в хранилище для файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="21b63-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="21b63-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="21b63-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="21b63-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="21b63-422">0x00200000</span></span>  <br/> |<span data-ttu-id="21b63-423">Если этот флаг установлен в [каноническом свойстве PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) упакованного PST-хранилища, это означает, что при поступлении в хранилище нового сообщения правила и фильтрация спама применяются для сообщения отдельно.</span><span class="sxs-lookup"><span data-stu-id="21b63-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="21b63-424">Затем хранилище вызывает метод [IMAPISupport::Notify](imapisupport-notify.md), задавая передаваемый параметр **fnevNewMail** в структуре [NOTIFICATION](notification.md), с отправкой сведений о новом сообщении прослушивающему клиенту.</span><span class="sxs-lookup"><span data-stu-id="21b63-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="21b63-425">Впоследствии, когда прослушивающий клиент получает уведомление, к сообщению не применяются правила.</span><span class="sxs-lookup"><span data-stu-id="21b63-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="21b63-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="21b63-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="21b63-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="21b63-427">0x00040000</span></span>  <br/> |<span data-ttu-id="21b63-428">Если этот флаг включен в [каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), это значит, что хранилище поддерживает хранилище Юникод.</span><span class="sxs-lookup"><span data-stu-id="21b63-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="21b63-429">Клиент можно проверить наличие флага, чтобы принять решение о запросе или сохранении сведений Юникода в хранилище.</span><span class="sxs-lookup"><span data-stu-id="21b63-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="21b63-430">Определения для архивации элементов в папке</span><span class="sxs-lookup"><span data-stu-id="21b63-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="21b63-431">Следующие определения констант — это значения, используемые для задания [канонического свойства PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="21b63-432">Определения для отображения удаленных объектов</span><span class="sxs-lookup"><span data-stu-id="21b63-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="21b63-433">Следующие определения констант и макросов предназначены для отображения удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="21b63-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="21b63-434">Дополнительные сведения см. в статье [Каноническое свойство PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="21b63-435">Определения для кодов ошибок адресной книги Exchange и хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="21b63-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="21b63-436">Ниже указаны определения кодов ошибок для адресной книги Exchange и хранилища сообщений с возможностью повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="21b63-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="21b63-437">Последний вызов отключенного глобального каталога (GC) может привести к ошибке **MAPI_E_END_OF_SESSION**, требующей выполнения повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="21b63-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="21b63-438">MAPI Outlook поддерживает повторное подключение к серверу GC без специальной перенастройки, но клиенту могут быть возвращены некоторые другие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="21b63-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="21b63-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="21b63-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="21b63-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="21b63-440">0x80040200</span></span>  <br/> |<span data-ttu-id="21b63-441">Возвращается, если соединение отключено.</span><span class="sxs-lookup"><span data-stu-id="21b63-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="21b63-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="21b63-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="21b63-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="21b63-443">0x80040125</span></span>  <br/> |<span data-ttu-id="21b63-444">Возвращается, если устарел маркер подключения удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="21b63-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="21b63-445">Если маркер текущей транзакции отличается от маркера подключения, это означает, что выполнено повторное подключение, поэтому возвращается параметр **MAPI_E_RECONNECTED**, который может обрабатываться аналогично параметру **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="21b63-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="21b63-446">Требуется повторная попытка вызова.</span><span class="sxs-lookup"><span data-stu-id="21b63-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="21b63-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="21b63-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="21b63-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="21b63-448">0x80040126</span></span>  <br/> |<span data-ttu-id="21b63-449">Возвращается при отсутствии подключения.</span><span class="sxs-lookup"><span data-stu-id="21b63-449">Returned when the connection is offline.</span></span> <span data-ttu-id="21b63-450">Обычно это означает какое-то происшествие в среде, например сбой сервера или отсутствие возможности подключения.</span><span class="sxs-lookup"><span data-stu-id="21b63-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="21b63-451">Эта ошибка чаще всего случается при использовании профиля в режиме кэширования и попытке обойти кэш для связи с сервером.</span><span class="sxs-lookup"><span data-stu-id="21b63-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="21b63-452">Если изначально отсутствовала возможность установки соединения кэша с сервером, он может быть в автономном состоянии, при котором может возникать ошибка **MAPI_E_OFFLINE**.</span><span class="sxs-lookup"><span data-stu-id="21b63-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="21b63-453">Никакая из предыдущих двух ошибок не возвращается в сценариях, в которых они подходят для применения.</span><span class="sxs-lookup"><span data-stu-id="21b63-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="21b63-454">В большинстве случаев возвращаются ошибки **MAPI\_E_NETWORK_ERROR** или **MAPI_E_CALL_FAILED**.</span><span class="sxs-lookup"><span data-stu-id="21b63-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="21b63-455">Ни одна из них не появляется при использовании загрузки для [клиента MAPI Microsoft Exchange Server и объектов данных совместной работы 1.2.1](https://support.microsoft.com/kb/171440).</span><span class="sxs-lookup"><span data-stu-id="21b63-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="21b63-456">Определения для квот режима кэширования почтовых ящиков Exchange Server</span><span class="sxs-lookup"><span data-stu-id="21b63-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="21b63-457">Следующие определения констант используются в Microsoft Outlook 2010 и Microsoft Outlook 2013, чтобы задавать квоты профиля в режиме кэширования Exchange, аналогичные квотам почтового ящика Exchange, которые в противном случае доступны только для профиля в сети.</span><span class="sxs-lookup"><span data-stu-id="21b63-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="21b63-458">Эти свойства сопоставляются с соответствующими сетевыми свойствами и содержат такие же значения в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="21b63-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="21b63-459">PR_QUOTA_WARNING сопоставляется с PR_STORAGE_QUOTA_LIMIT PR_QUOTA_SEND с PR_QUOTA_PROHIBIT_SEND_QUOTA и PR_QUOTA_RECEIVE с PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="21b63-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="21b63-460">Определения для формата сообщения</span><span class="sxs-lookup"><span data-stu-id="21b63-460">Definitions for message format</span></span>

<span data-ttu-id="21b63-461">Следующие определения констант — это значения, которые используются для задания [канонического свойства PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="21b63-462">Определения для использования протокола RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="21b63-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="21b63-463">Определения констант, используемые в качестве флагов для задания свойства, см. в разделе [Каноническое свойство PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="21b63-464">Определения констант, используемые для задания свойства, см. в разделе [Каноническое свойство PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="21b63-465">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="21b63-465">Identifiers</span></span>

<span data-ttu-id="21b63-466">Связывайте следующие символьные имена GUID с их значениями с помощью макроса `DEFINE_OLEGUID`, заданного в файле заголовка guiddef.h пакета средств разработки программного обеспечения (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="21b63-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="21b63-467">Следующий идентификатор предназначен для раздела профиля Capone адресной книги, который для поддержки нескольких почтовых ящиков Exchange ([MultiEx](using-multiple-exchange-accounts.md)) содержит свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md), эффективно отключающее контейнер по умолчанию, заданный с помощью [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="21b63-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="21b63-468">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="21b63-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="21b63-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="21b63-469">IMAPISync : SynchronizeInBackground</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="21b63-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="21b63-470">IMAPISyncProgressCallback::Done</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="21b63-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="21b63-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="21b63-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="21b63-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="21b63-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="21b63-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="21b63-474">Идентификаторы интерфейсов обработчика переопределения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="21b63-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="21b63-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="21b63-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="21b63-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="21b63-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="21b63-477">См. также</span><span class="sxs-lookup"><span data-stu-id="21b63-477">See also</span></span>

- [<span data-ttu-id="21b63-478">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="21b63-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="21b63-479">Сведения об именованных свойствах, используемых в Outlook</span><span class="sxs-lookup"><span data-stu-id="21b63-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="21b63-480">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="21b63-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="21b63-481">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="21b63-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="21b63-482">Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="21b63-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

