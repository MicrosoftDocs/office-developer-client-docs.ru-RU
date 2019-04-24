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
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321296"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="bab07-103">Каноническое свойство PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="bab07-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="bab07-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bab07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bab07-105">Содержит **идентификаторами EntryID** делегатов.</span><span class="sxs-lookup"><span data-stu-id="bab07-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bab07-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bab07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bab07-107">ПР_СЧДИНФО_ДЕЛЕГАТЕ_ЕНТРИДС</span><span class="sxs-lookup"><span data-stu-id="bab07-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="bab07-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bab07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bab07-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="bab07-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="bab07-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bab07-110">Data type:</span></span>  <br/> |<span data-ttu-id="bab07-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab07-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bab07-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bab07-112">Area:</span></span>  <br/> |<span data-ttu-id="bab07-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="bab07-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bab07-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bab07-114">Remarks</span></span>

<span data-ttu-id="bab07-115">Каждая запись должна содержать значение свойства **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) каждой записи адресной книги делегата.</span><span class="sxs-lookup"><span data-stu-id="bab07-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="bab07-116">Это свойство должно быть задано в объекте сведений о делегате.</span><span class="sxs-lookup"><span data-stu-id="bab07-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bab07-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bab07-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bab07-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bab07-118">Protocol specifications</span></span>

<span data-ttu-id="bab07-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab07-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab07-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bab07-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bab07-121">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab07-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab07-122">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="bab07-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bab07-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="bab07-123">Header files</span></span>

<span data-ttu-id="bab07-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bab07-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bab07-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bab07-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bab07-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="bab07-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bab07-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="bab07-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bab07-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bab07-128">See also</span></span>



[<span data-ttu-id="bab07-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bab07-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bab07-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bab07-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bab07-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bab07-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bab07-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bab07-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

