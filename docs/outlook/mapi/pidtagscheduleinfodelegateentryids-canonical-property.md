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
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811830"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="41890-103">Каноническое свойство PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="41890-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="41890-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41890-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41890-105">Содержит **EntryIDs** делегатов.</span><span class="sxs-lookup"><span data-stu-id="41890-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41890-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="41890-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41890-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="41890-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="41890-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="41890-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41890-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="41890-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="41890-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="41890-110">Data type:</span></span>  <br/> |<span data-ttu-id="41890-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="41890-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="41890-112">Область:</span><span class="sxs-lookup"><span data-stu-id="41890-112">Area:</span></span>  <br/> |<span data-ttu-id="41890-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="41890-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41890-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="41890-114">Remarks</span></span>

<span data-ttu-id="41890-115">Каждая запись должна содержать значение свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) каждого делегата записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="41890-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="41890-116">Это свойство необходимо установить в объекте сведения делегата.</span><span class="sxs-lookup"><span data-stu-id="41890-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41890-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41890-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41890-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="41890-118">Protocol specifications</span></span>

<span data-ttu-id="41890-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41890-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41890-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="41890-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41890-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41890-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41890-122">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="41890-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41890-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="41890-123">Header files</span></span>

<span data-ttu-id="41890-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41890-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="41890-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="41890-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="41890-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41890-126">Mapitags.h</span></span>
  
> <span data-ttu-id="41890-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="41890-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41890-128">См. также</span><span class="sxs-lookup"><span data-stu-id="41890-128">See also</span></span>



[<span data-ttu-id="41890-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41890-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41890-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41890-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41890-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="41890-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41890-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="41890-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

