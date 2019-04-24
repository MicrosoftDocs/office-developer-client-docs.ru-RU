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
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="bfe27-103">Каноническое свойство PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="bfe27-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="bfe27-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe27-105">Задает список идентификаторами EntryID объектов, соответствующих членам личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="bfe27-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe27-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bfe27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfe27-107">Диспиддлмемберс</span><span class="sxs-lookup"><span data-stu-id="bfe27-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="bfe27-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="bfe27-108">Property set:</span></span>  <br/> |<span data-ttu-id="bfe27-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="bfe27-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bfe27-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="bfe27-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bfe27-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="bfe27-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="bfe27-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bfe27-112">Data type:</span></span>  <br/> |<span data-ttu-id="bfe27-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfe27-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bfe27-114">Область:</span><span class="sxs-lookup"><span data-stu-id="bfe27-114">Area:</span></span>  <br/> |<span data-ttu-id="bfe27-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="bfe27-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe27-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfe27-116">Remarks</span></span>

<span data-ttu-id="bfe27-117">Участники личного списка рассылки могут быть другими личными списками рассылки, электронными адресами, входящими в контакт, глобальными списками адресов пользователей или списками рассылки или одноразовыми адресами электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bfe27-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="bfe27-118">Формат каждого EntryId должен быть либо одноразовым EntryIdом, указанным в разделе [[MS – окскдата],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) либо упакованным entryidм.</span><span class="sxs-lookup"><span data-stu-id="bfe27-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="bfe27-119">При задании этого свойства клиент или сервер должны обеспечивать его общий размер менее 15 000 байт.</span><span class="sxs-lookup"><span data-stu-id="bfe27-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="bfe27-120">Это свойство указывает список одноразовых идентификаторами EntryID, соответствующих членам личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="bfe27-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="bfe27-121">Эти одноразовые идентификаторами EntryID инкапсулируют отображаемые имена и адреса электронной почты для участников личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="bfe27-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="bfe27-122">Если клиент или сервер задают значение этого свойства, его необходимо синхронизировать с этим свойством **диспиддлмемберс** для каждой записи в свойстве **диспиддлонеоффмемберс** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), так как должна быть запись в элементе одно и то же положение в **диспиддлонеоффмемберс**.</span><span class="sxs-lookup"><span data-stu-id="bfe27-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bfe27-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bfe27-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfe27-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bfe27-124">Protocol specifications</span></span>

<span data-ttu-id="bfe27-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe27-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe27-126">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bfe27-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfe27-127">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe27-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe27-128">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="bfe27-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfe27-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="bfe27-129">Header files</span></span>

<span data-ttu-id="bfe27-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bfe27-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfe27-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bfe27-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfe27-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bfe27-132">See also</span></span>



[<span data-ttu-id="bfe27-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe27-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfe27-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe27-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfe27-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe27-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfe27-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bfe27-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

