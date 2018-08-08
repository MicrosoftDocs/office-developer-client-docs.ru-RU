---
title: Каноническое свойство PidLidOriginalStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOriginalStoreEntryId
api_type:
- COM
ms.assetid: 1b1fc008-9cd5-49f6-9f91-b59e305a1e82
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aaf442b941cfe14f695bf5e7f7ec246d06e5ae0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810445"
---
# <a name="pidlidoriginalstoreentryid-canonical-property"></a><span data-ttu-id="d56d2-103">Каноническое свойство PidLidOriginalStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="d56d2-103">PidLidOriginalStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d56d2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d56d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d56d2-105">Указывает идентификатор записи хранилища сотрудника.</span><span class="sxs-lookup"><span data-stu-id="d56d2-105">Specifies the entry ID of the delegator's store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d56d2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d56d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d56d2-107">dispidOrigStoreEid</span><span class="sxs-lookup"><span data-stu-id="d56d2-107">dispidOrigStoreEid</span></span>  <br/> |
|<span data-ttu-id="d56d2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d56d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="d56d2-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d56d2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d56d2-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d56d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d56d2-111">0x00008237</span><span class="sxs-lookup"><span data-stu-id="d56d2-111">0x00008237</span></span>  <br/> |
|<span data-ttu-id="d56d2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d56d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="d56d2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d56d2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d56d2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d56d2-114">Area:</span></span>  <br/> |<span data-ttu-id="d56d2-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="d56d2-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d56d2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d56d2-116">Remarks</span></span>

<span data-ttu-id="d56d2-117">Это свойство необходимо задать на собрание объекты, которые были созданы или изменены с делегатом.</span><span class="sxs-lookup"><span data-stu-id="d56d2-117">This property should be set on meeting objects which have been created or updated by a delegate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d56d2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d56d2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d56d2-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d56d2-119">Protocol specifications</span></span>

<span data-ttu-id="d56d2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d56d2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d56d2-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d56d2-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d56d2-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d56d2-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="d56d2-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d56d2-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d56d2-124">Header files</span></span>

<span data-ttu-id="d56d2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d56d2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d56d2-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d56d2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d56d2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d56d2-127">See also</span></span>



[<span data-ttu-id="d56d2-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d56d2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d56d2-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d56d2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d56d2-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d56d2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d56d2-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d56d2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

