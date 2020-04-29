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
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="3f9f7-103">Каноническое свойство PidTagRemindersOnlineEntryId</span><span class="sxs-lookup"><span data-stu-id="3f9f7-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3f9f7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f9f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f9f7-105">Содержит идентификатор **EntryID** папки напоминаний.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f9f7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3f9f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f9f7-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3f9f7-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3f9f7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3f9f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f9f7-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="3f9f7-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="3f9f7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3f9f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f9f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f9f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f9f7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3f9f7-112">Area:</span></span>  <br/> |<span data-ttu-id="3f9f7-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9f7-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f9f7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f9f7-114">Remarks</span></span>

<span data-ttu-id="3f9f7-115">Это свойство хранится в папке "Входящие" и в корневой папке хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="3f9f7-116">Чтобы получить доступ к свойству в определенном хранилище сообщений, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="3f9f7-117">Сначала найдите свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="3f9f7-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="3f9f7-118">Используйте [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) , чтобы получить ссылку на **EntryID** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="3f9f7-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="3f9f7-119">Если **IMsgStore:: жетрецеивефолдер** — успешно, используйте ссылку на идентификатор **EntryID** папки "Входящие" и [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть папку "Входящие" и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="3f9f7-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="3f9f7-120">Если **IMsgStore:: OpenEntry** — успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и [IMAPIProp::-PROPS](imapiprop-getprops.md) , чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="3f9f7-121">Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="3f9f7-122">Для этого используйте **IMsgStore:: OpenEntry**, УКАЗАВ значение NULL для **лпентрид**, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="3f9f7-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="3f9f7-123">При успешном открытии корневой папки используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::-PROPS** , чтобы получить нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="3f9f7-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f9f7-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f9f7-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3f9f7-125">Protocol specifications</span></span>

<span data-ttu-id="3f9f7-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f9f7-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f9f7-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3f9f7-128">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f9f7-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f9f7-129">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f9f7-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3f9f7-130">Header files</span></span>

<span data-ttu-id="3f9f7-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3f9f7-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f9f7-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f9f7-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="3f9f7-133">Mapitags.h</span></span>
  
> <span data-ttu-id="3f9f7-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="3f9f7-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f9f7-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3f9f7-135">See also</span></span>



[<span data-ttu-id="3f9f7-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9f7-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f9f7-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9f7-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f9f7-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9f7-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f9f7-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3f9f7-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

