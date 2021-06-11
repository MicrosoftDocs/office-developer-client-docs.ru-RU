---
title: Каноническое свойство PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335051"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="2ed81-103">Каноническое свойство PidLidDistributionListOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="2ed81-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="2ed81-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ed81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ed81-105">Указывает список разных entryIds, которые соответствуют членам личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="2ed81-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ed81-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ed81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ed81-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="2ed81-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="2ed81-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2ed81-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ed81-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="2ed81-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="2ed81-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2ed81-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2ed81-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="2ed81-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="2ed81-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ed81-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ed81-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ed81-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ed81-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2ed81-114">Area:</span></span>  <br/> |<span data-ttu-id="2ed81-115">Contact</span><span class="sxs-lookup"><span data-stu-id="2ed81-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ed81-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ed81-116">Remarks</span></span>

<span data-ttu-id="2ed81-117">Эти разовый EntryIds инкапсулируют имена и адреса электронной почты личных участников списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="2ed81-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="2ed81-118">Если клиент или сервер задают это свойство, оно должно синхронизироваться с свойством **dispidDLMembers** [(PidLidDistributionListMembers).](pidliddistributionlistmembers-canonical-property.md)Для каждой записи в свойстве **dispidDLOneOffMembers** должна быть запись в том же положении в свойстве **dispidDLMembers.**</span><span class="sxs-lookup"><span data-stu-id="2ed81-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="2ed81-119">При настройке **dispidDLOneOffMembers** клиент или сервер должны убедиться, что его общий размер не превышает 15 000 bytes в размере.</span><span class="sxs-lookup"><span data-stu-id="2ed81-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ed81-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ed81-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ed81-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2ed81-121">Protocol specifications</span></span>

<span data-ttu-id="2ed81-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ed81-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ed81-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2ed81-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ed81-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ed81-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ed81-125">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="2ed81-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ed81-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="2ed81-126">Header files</span></span>

<span data-ttu-id="2ed81-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ed81-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ed81-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ed81-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ed81-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2ed81-129">See also</span></span>



[<span data-ttu-id="2ed81-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed81-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ed81-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed81-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ed81-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed81-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ed81-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="2ed81-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

