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
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335072"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="ffcfc-103">Каноническое свойство PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="ffcfc-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="ffcfc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffcfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffcfc-105">Указывает список entryIds объектов, которые соответствуют членам личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffcfc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ffcfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffcfc-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="ffcfc-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="ffcfc-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ffcfc-108">Property set:</span></span>  <br/> |<span data-ttu-id="ffcfc-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ffcfc-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ffcfc-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ffcfc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ffcfc-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="ffcfc-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="ffcfc-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ffcfc-112">Data type:</span></span>  <br/> |<span data-ttu-id="ffcfc-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="ffcfc-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="ffcfc-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ffcfc-114">Area:</span></span>  <br/> |<span data-ttu-id="ffcfc-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="ffcfc-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffcfc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ffcfc-116">Remarks</span></span>

<span data-ttu-id="ffcfc-117">Участниками личного списка рассылки могут быть другие личные списки рассылки, электронные адреса, содержащиеся в контакте, пользователи глобального списка адресов или списки рассылки, а также односетные адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="ffcfc-118">Форматом каждого EntryId должен быть однофайловый EntryId, указанный [в [MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) или завернутый EntryId.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="ffcfc-119">При установке этого свойства клиент или сервер должны убедиться, что его общий размер не превышает 15 000.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="ffcfc-120">Это свойство указывает список одновключенных entryId, которые соответствуют членам личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="ffcfc-121">Эти однофакторные коды EntryId инкапсулируют отображаемую и электронную почту участников списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="ffcfc-122">Если клиент или сервер установили это свойство, оно должно быть синхронизировано с этим свойством **dispidDLMembers** для каждой записи в свойстве **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers),](pidliddistributionlistoneoffmembers-canonical-property.md)должна быть запись в той же позиции в **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffcfc-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ffcfc-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffcfc-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ffcfc-124">Protocol specifications</span></span>

<span data-ttu-id="ffcfc-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffcfc-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffcfc-126">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffcfc-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffcfc-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffcfc-128">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffcfc-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ffcfc-129">Header files</span></span>

<span data-ttu-id="ffcfc-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffcfc-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffcfc-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ffcfc-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffcfc-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ffcfc-132">See also</span></span>



[<span data-ttu-id="ffcfc-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcfc-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffcfc-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcfc-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffcfc-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcfc-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffcfc-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ffcfc-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

