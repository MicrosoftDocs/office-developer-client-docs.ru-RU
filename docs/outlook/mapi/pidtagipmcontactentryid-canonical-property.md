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
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="09ff2-103">Каноническое свойство PidTagIpmContactEntryId</span><span class="sxs-lookup"><span data-stu-id="09ff2-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="09ff2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09ff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09ff2-105">Содержит идентификатор \*\*\*\* папки контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="09ff2-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09ff2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="09ff2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09ff2-107">ПР_ИПМ_КОНТАКТ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="09ff2-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="09ff2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="09ff2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09ff2-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="09ff2-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="09ff2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="09ff2-110">Data type:</span></span>  <br/> |<span data-ttu-id="09ff2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="09ff2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="09ff2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="09ff2-112">Area:</span></span>  <br/> |<span data-ttu-id="09ff2-113">Folder</span><span class="sxs-lookup"><span data-stu-id="09ff2-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09ff2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09ff2-114">Remarks</span></span>

<span data-ttu-id="09ff2-115">Это свойство хранится в папке "Входящие" и в корневой папке хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="09ff2-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="09ff2-116">Чтобы получить доступ к свойству в определенном хранилище сообщений, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09ff2-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="09ff2-117">Сначала найдите свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="09ff2-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="09ff2-118">Используйте **IMsgStore:: жетрецеивефолдер** , чтобы получить ссылку на **EntryID** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="09ff2-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="09ff2-119">Если **IMsgStore:: жетрецеивефолдер** — успешно, используйте ссылку на идентификатор **EntryID** папки "Входящие" и **IMsgStore:: OpenEntry** , чтобы открыть папку "Входящие" и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="09ff2-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="09ff2-120">Если **IMsgStore:: OpenEntry** — успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::** -Props, чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="09ff2-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="09ff2-121">Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="09ff2-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="09ff2-122">Для этого используйте **IMsgStore:: OpenEntry**, УКАЗАВ значение NULL для \* \* лпентрид \* \*, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="09ff2-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="09ff2-123">При успешном открытии корневой папки используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::** -Props, чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="09ff2-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="09ff2-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09ff2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09ff2-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="09ff2-125">Protocol specifications</span></span>

<span data-ttu-id="09ff2-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09ff2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09ff2-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="09ff2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09ff2-128">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09ff2-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09ff2-129">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="09ff2-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="09ff2-130">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09ff2-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09ff2-131">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="09ff2-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09ff2-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="09ff2-132">Header files</span></span>

<span data-ttu-id="09ff2-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="09ff2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="09ff2-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="09ff2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="09ff2-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="09ff2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="09ff2-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="09ff2-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09ff2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="09ff2-137">See also</span></span>



[<span data-ttu-id="09ff2-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="09ff2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09ff2-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="09ff2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09ff2-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="09ff2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09ff2-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="09ff2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

