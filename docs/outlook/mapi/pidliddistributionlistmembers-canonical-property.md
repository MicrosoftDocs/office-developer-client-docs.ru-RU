---
title: Каноническое свойство PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9bfb94b2929f780a428fb932efb3538f94f5aaea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591466"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="74de9-103">Каноническое свойство PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="74de9-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="74de9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74de9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74de9-105">Задает список EntryIds объектов, которые соответствуют членов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="74de9-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74de9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="74de9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74de9-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="74de9-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="74de9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="74de9-108">Property set:</span></span>  <br/> |<span data-ttu-id="74de9-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="74de9-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="74de9-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="74de9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="74de9-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="74de9-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="74de9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="74de9-112">Data type:</span></span>  <br/> |<span data-ttu-id="74de9-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="74de9-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="74de9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="74de9-114">Area:</span></span>  <br/> |<span data-ttu-id="74de9-115">Contact</span><span class="sxs-lookup"><span data-stu-id="74de9-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74de9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="74de9-116">Remarks</span></span>

<span data-ttu-id="74de9-117">Члены списка рассылки может быть другие списки рассылки, содержащихся в контакт, пользователи глобального списка адресов или списки рассылки или адреса электронной почты одноразовых электронных адресов.</span><span class="sxs-lookup"><span data-stu-id="74de9-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="74de9-118">Формат каждого EntryId должен быть одноразовых EntryId, как указано в [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) или оболочку EntryId.</span><span class="sxs-lookup"><span data-stu-id="74de9-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="74de9-119">Если для свойства, клиент или сервер необходимо убедиться, что его общий размер составляет менее 15 000 байт.</span><span class="sxs-lookup"><span data-stu-id="74de9-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="74de9-120">Это свойство определяет список единичных записей, соответствующих членов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="74de9-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="74de9-121">Эти единичных записей инкапсулируют отображаемые имена и адреса электронной почты из личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="74de9-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="74de9-122">Если этому свойству присвоено клиент или сервер, его необходимо синхронизировать с этой свойство **dispidDLMembers** для каждой записи в свойстве **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), должна быть запись в же позиции в **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="74de9-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74de9-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="74de9-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74de9-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="74de9-124">Protocol specifications</span></span>

<span data-ttu-id="74de9-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74de9-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74de9-126">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="74de9-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74de9-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74de9-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74de9-128">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="74de9-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74de9-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="74de9-129">Header files</span></span>

<span data-ttu-id="74de9-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74de9-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="74de9-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="74de9-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74de9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="74de9-132">See also</span></span>



[<span data-ttu-id="74de9-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74de9-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74de9-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74de9-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74de9-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="74de9-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74de9-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="74de9-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

