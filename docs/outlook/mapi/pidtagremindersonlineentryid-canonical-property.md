---
title: Каноническое свойство PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d845a37f9248a30dadd4db7722d8bed0f9f8d264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355064"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="75071-103">Каноническое свойство PidTagRemindersOnlineEntryId</span><span class="sxs-lookup"><span data-stu-id="75071-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="75071-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75071-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75071-105">Содержит **EntryID** папки напоминаний.</span><span class="sxs-lookup"><span data-stu-id="75071-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75071-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="75071-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75071-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="75071-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="75071-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="75071-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75071-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="75071-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="75071-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="75071-110">Data type:</span></span>  <br/> |<span data-ttu-id="75071-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75071-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75071-112">Область:</span><span class="sxs-lookup"><span data-stu-id="75071-112">Area:</span></span>  <br/> |<span data-ttu-id="75071-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="75071-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75071-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="75071-114">Remarks</span></span>

<span data-ttu-id="75071-115">Это свойство хранится в папке "Входящие" и в корневой папке в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="75071-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="75071-116">Чтобы получить доступ к свойству в определенном хранилище сообщений, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="75071-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="75071-117">Сначала наберем свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="75071-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="75071-118">Используйте [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить ссылку на **EntryID** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="75071-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="75071-119">Если **IMsgStore::GetReceiveFolder** успешно, используйте ссылку на **EntryID** входящих сообщений и [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть "Входящие" и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="75071-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="75071-120">Если **IMsgStore::OpenEntry** успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="75071-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="75071-121">Если шаг 1, 2 или 3 не удается, наберем свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="75071-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="75071-122">Для этого используйте **IMsgStore::OpenEntry,** указав NULL для **lpEntryID,** чтобы открыть корневую папку в хранилище сообщений и получить ссылку на объект **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="75071-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="75071-123">Если открытие корневой папки успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps,** чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="75071-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="75071-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75071-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75071-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="75071-125">Protocol specifications</span></span>

<span data-ttu-id="75071-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75071-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75071-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="75071-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75071-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75071-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75071-129">Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="75071-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75071-130">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="75071-130">Header files</span></span>

<span data-ttu-id="75071-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75071-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="75071-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="75071-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="75071-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75071-133">Mapitags.h</span></span>
  
> <span data-ttu-id="75071-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="75071-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75071-135">См. также</span><span class="sxs-lookup"><span data-stu-id="75071-135">See also</span></span>



[<span data-ttu-id="75071-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75071-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75071-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75071-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75071-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="75071-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75071-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="75071-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

