---
title: Каноническое свойство PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314940"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="c7c05-103">Каноническое свойство PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="c7c05-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="c7c05-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7c05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7c05-105">Содержит имена делегатов.</span><span class="sxs-lookup"><span data-stu-id="c7c05-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7c05-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c7c05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7c05-107">ПР_СЧДИНФО_ДЕЛЕГАТЕ_НАМЕС, ПР_СЧДИНФО_ДЕЛЕГАТЕ_НАМЕС_А, ПР_СЧДИНФО_ДЕЛЕГАТЕ_НАМЕС_В</span><span class="sxs-lookup"><span data-stu-id="c7c05-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="c7c05-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c7c05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7c05-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="c7c05-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="c7c05-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c7c05-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7c05-111">PT_MV_STRING8, ПТ_МВ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="c7c05-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c7c05-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c7c05-112">Area:</span></span>  <br/> |<span data-ttu-id="c7c05-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="c7c05-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7c05-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7c05-114">Remarks</span></span>

<span data-ttu-id="c7c05-115">Каждая запись в этих свойствах должна содержать значение свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) каждой адресной книги делегата.</span><span class="sxs-lookup"><span data-stu-id="c7c05-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7c05-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c7c05-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7c05-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c7c05-117">Protocol specifications</span></span>

<span data-ttu-id="c7c05-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c05-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c05-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c7c05-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7c05-120">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c05-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c05-121">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7c05-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7c05-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c7c05-122">Header files</span></span>

<span data-ttu-id="c7c05-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c7c05-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7c05-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c7c05-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7c05-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c7c05-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c7c05-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c7c05-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7c05-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c7c05-127">See also</span></span>



[<span data-ttu-id="c7c05-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c7c05-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7c05-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c7c05-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7c05-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c7c05-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7c05-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c7c05-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

