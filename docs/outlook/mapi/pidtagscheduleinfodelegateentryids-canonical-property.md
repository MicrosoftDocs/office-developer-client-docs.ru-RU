---
title: Каноническое свойство PidTagScheduleInfoDelegateEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f7521d387fa45c191a67f2a20320fac700baed37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567218"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="b5dbd-103">Каноническое свойство PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="b5dbd-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="b5dbd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5dbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5dbd-105">Содержит **EntryIDs** делегатов.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5dbd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b5dbd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5dbd-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="b5dbd-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="b5dbd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b5dbd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5dbd-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="b5dbd-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="b5dbd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b5dbd-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5dbd-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b5dbd-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="b5dbd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b5dbd-112">Area:</span></span>  <br/> |<span data-ttu-id="b5dbd-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="b5dbd-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5dbd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5dbd-114">Remarks</span></span>

<span data-ttu-id="b5dbd-115">Каждая запись должна содержать значение свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) каждого делегата записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="b5dbd-116">Это свойство необходимо установить в объекте сведения делегата.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5dbd-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5dbd-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5dbd-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b5dbd-118">Protocol specifications</span></span>

<span data-ttu-id="b5dbd-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5dbd-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5dbd-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5dbd-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5dbd-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5dbd-122">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5dbd-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b5dbd-123">Header files</span></span>

<span data-ttu-id="b5dbd-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5dbd-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5dbd-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5dbd-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5dbd-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b5dbd-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b5dbd-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5dbd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b5dbd-128">See also</span></span>



[<span data-ttu-id="b5dbd-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5dbd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5dbd-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5dbd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5dbd-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b5dbd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5dbd-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b5dbd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

