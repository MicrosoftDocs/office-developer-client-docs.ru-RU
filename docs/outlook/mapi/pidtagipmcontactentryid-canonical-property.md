---
title: Каноническое свойство PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327904"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="01a61-103">Каноническое свойство PidTagIpmContactEntryId</span><span class="sxs-lookup"><span data-stu-id="01a61-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="01a61-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01a61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01a61-105">Содержит **entryID** папки Outlook контактов.</span><span class="sxs-lookup"><span data-stu-id="01a61-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01a61-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01a61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01a61-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="01a61-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="01a61-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01a61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01a61-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="01a61-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="01a61-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01a61-110">Data type:</span></span>  <br/> |<span data-ttu-id="01a61-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="01a61-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="01a61-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01a61-112">Area:</span></span>  <br/> |<span data-ttu-id="01a61-113">Folder</span><span class="sxs-lookup"><span data-stu-id="01a61-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01a61-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="01a61-114">Remarks</span></span>

<span data-ttu-id="01a61-115">Это свойство хранится в папке "Входящие" и в корневой папке магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="01a61-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="01a61-116">Чтобы получить доступ к свойству в определенном хранилище сообщений, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="01a61-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="01a61-117">Сначала найми свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="01a61-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="01a61-118">Используйте **IMsgStore::GetReceiveFolder,** чтобы получить ссылку на **EntryID** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="01a61-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="01a61-119">Если **IMsgStore::GetReceiveFolder** успешно, используйте ссылку на **EntryID** почтового ящика и **IMsgStore::OpenEntry,** чтобы открыть почтовый ящик и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="01a61-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="01a61-120">Если **IMsgStore::OpenEntry** успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужного свойства.</span><span class="sxs-lookup"><span data-stu-id="01a61-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="01a61-121">Если не удается сделать шаг 1, 2 или 3, и посмотрите свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="01a61-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="01a61-122">Для этого используйте **IMsgStore::OpenEntry** с указанием NULL для \*\* lpEntryID \*\*, чтобы открыть корневую папку магазина сообщений и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="01a61-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="01a61-123">Если открытие корневой папки успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужного свойства.</span><span class="sxs-lookup"><span data-stu-id="01a61-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="01a61-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01a61-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01a61-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01a61-125">Protocol specifications</span></span>

<span data-ttu-id="01a61-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01a61-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01a61-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="01a61-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01a61-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01a61-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01a61-129">Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="01a61-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="01a61-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01a61-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01a61-131">Указывает методы подключения к почтовым ящикам и настройки их в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="01a61-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01a61-132">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="01a61-132">Header files</span></span>

<span data-ttu-id="01a61-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01a61-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="01a61-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01a61-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="01a61-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01a61-135">Mapitags.h</span></span>
  
> <span data-ttu-id="01a61-136">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="01a61-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01a61-137">См. также</span><span class="sxs-lookup"><span data-stu-id="01a61-137">See also</span></span>



[<span data-ttu-id="01a61-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01a61-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01a61-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01a61-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01a61-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01a61-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01a61-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="01a61-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

