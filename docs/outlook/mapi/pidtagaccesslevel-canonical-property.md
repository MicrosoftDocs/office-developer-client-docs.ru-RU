---
title: Каноническое свойство PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331999"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="8afbc-103">Каноническое свойство PidTagAccessLevel</span><span class="sxs-lookup"><span data-stu-id="8afbc-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="8afbc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8afbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8afbc-105">Указывает уровень доступа клиента к объекту.</span><span class="sxs-lookup"><span data-stu-id="8afbc-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8afbc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8afbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8afbc-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="8afbc-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="8afbc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8afbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8afbc-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="8afbc-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="8afbc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8afbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="8afbc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8afbc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8afbc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8afbc-112">Area:</span></span>  <br/> |<span data-ttu-id="8afbc-113">Свойства управления доступом</span><span class="sxs-lookup"><span data-stu-id="8afbc-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8afbc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8afbc-114">Remarks</span></span>

<span data-ttu-id="8afbc-115">Это свойство для клиента только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8afbc-115">This property is read-only for the client.</span></span> <span data-ttu-id="8afbc-116">Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8afbc-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="8afbc-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8afbc-117">**Value**</span></span>|<span data-ttu-id="8afbc-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8afbc-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8afbc-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8afbc-119">0x00000000</span></span>  <br/> |<span data-ttu-id="8afbc-120">Только чтение</span><span class="sxs-lookup"><span data-stu-id="8afbc-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="8afbc-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8afbc-121">0x00000001</span></span>  <br/> |<span data-ttu-id="8afbc-122">Изменение</span><span class="sxs-lookup"><span data-stu-id="8afbc-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8afbc-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8afbc-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8afbc-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8afbc-124">Protocol specifications</span></span>

<span data-ttu-id="8afbc-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8afbc-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8afbc-126">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8afbc-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8afbc-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8afbc-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8afbc-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="8afbc-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8afbc-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="8afbc-129">Header files</span></span>

<span data-ttu-id="8afbc-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8afbc-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="8afbc-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8afbc-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="8afbc-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8afbc-132">Mapitags.h</span></span>
  
> <span data-ttu-id="8afbc-133">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="8afbc-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8afbc-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8afbc-134">See also</span></span>



[<span data-ttu-id="8afbc-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8afbc-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8afbc-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8afbc-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8afbc-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8afbc-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8afbc-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8afbc-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

