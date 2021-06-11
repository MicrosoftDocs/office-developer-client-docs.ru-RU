---
title: Каноническое свойство PidTagIpmAppointmentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327918"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a><span data-ttu-id="d0ac0-103">Каноническое свойство PidTagIpmAppointmentEntryId</span><span class="sxs-lookup"><span data-stu-id="d0ac0-103">PidTagIpmAppointmentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d0ac0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0ac0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0ac0-105">Содержит **entryID** папки Календарь Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-105">Contains the **EntryID** of the Outlook Calendar folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0ac0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d0ac0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0ac0-107">PR_IPM_APPOINTMENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d0ac0-107">PR_IPM_APPOINTMENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d0ac0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d0ac0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0ac0-109">0x36D0</span><span class="sxs-lookup"><span data-stu-id="d0ac0-109">0x36D0</span></span>  <br/> |
|<span data-ttu-id="d0ac0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d0ac0-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0ac0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d0ac0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d0ac0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d0ac0-112">Area:</span></span>  <br/> |<span data-ttu-id="d0ac0-113">Folder</span><span class="sxs-lookup"><span data-stu-id="d0ac0-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0ac0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0ac0-114">Remarks</span></span>

<span data-ttu-id="d0ac0-115">Это свойство хранится в папке "Входящие" и в корневой папке магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="d0ac0-116">Чтобы получить доступ к свойству в определенном хранилище сообщений, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="d0ac0-117">Сначала найми свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="d0ac0-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="d0ac0-118">Используйте [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить ссылку на **EntryID** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="d0ac0-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="d0ac0-119">Если **IMsgStore::GetReceiveFolder** успешно, используйте ссылку на **EntryID** почтового ящика и [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть почтовый ящик и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="d0ac0-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="d0ac0-120">Если **IMsgStore::OpenEntry** успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps](imapiprop-getprops.md) для получения нужного свойства.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="d0ac0-121">Если не удается сделать шаг 1, 2 или 3, и посмотрите свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="d0ac0-122">Для этого используйте **IMsgStore::OpenEntry,** указав NULL для **lpEntryID,** чтобы открыть корневую папку магазина сообщений и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="d0ac0-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="d0ac0-123">Если открытие корневой папки успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужного свойства.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="d0ac0-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d0ac0-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0ac0-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d0ac0-125">Protocol specifications</span></span>

<span data-ttu-id="d0ac0-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0ac0-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0ac0-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0ac0-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0ac0-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0ac0-129">Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0ac0-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d0ac0-130">Header files</span></span>

<span data-ttu-id="d0ac0-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0ac0-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0ac0-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0ac0-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0ac0-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d0ac0-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d0ac0-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0ac0-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d0ac0-135">See also</span></span>



[<span data-ttu-id="d0ac0-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0ac0-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0ac0-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0ac0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0ac0-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d0ac0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0ac0-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d0ac0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

