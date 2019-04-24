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
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="32ab0-103">Каноническое свойство PidTagAccessLevel</span><span class="sxs-lookup"><span data-stu-id="32ab0-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="32ab0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32ab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32ab0-105">Указывает уровень доступа клиента к объекту.</span><span class="sxs-lookup"><span data-stu-id="32ab0-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32ab0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="32ab0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32ab0-107">ПР_АКЦЕСС_ЛЕВЕЛ</span><span class="sxs-lookup"><span data-stu-id="32ab0-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="32ab0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="32ab0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32ab0-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="32ab0-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="32ab0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="32ab0-110">Data type:</span></span>  <br/> |<span data-ttu-id="32ab0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="32ab0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="32ab0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="32ab0-112">Area:</span></span>  <br/> |<span data-ttu-id="32ab0-113">Свойства управления доступом</span><span class="sxs-lookup"><span data-stu-id="32ab0-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32ab0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32ab0-114">Remarks</span></span>

<span data-ttu-id="32ab0-115">Для клиента это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="32ab0-115">This property is read-only for the client.</span></span> <span data-ttu-id="32ab0-116">Он должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="32ab0-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="32ab0-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="32ab0-117">**Value**</span></span>|<span data-ttu-id="32ab0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32ab0-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ab0-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32ab0-119">0x00000000</span></span>  <br/> |<span data-ttu-id="32ab0-120">Только чтение</span><span class="sxs-lookup"><span data-stu-id="32ab0-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="32ab0-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="32ab0-121">0x00000001</span></span>  <br/> |<span data-ttu-id="32ab0-122">Изменение</span><span class="sxs-lookup"><span data-stu-id="32ab0-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="32ab0-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="32ab0-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32ab0-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="32ab0-124">Protocol specifications</span></span>

<span data-ttu-id="32ab0-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ab0-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ab0-126">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="32ab0-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32ab0-127">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ab0-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ab0-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="32ab0-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32ab0-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="32ab0-129">Header files</span></span>

<span data-ttu-id="32ab0-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="32ab0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="32ab0-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="32ab0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="32ab0-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="32ab0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="32ab0-133">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="32ab0-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32ab0-134">См. также</span><span class="sxs-lookup"><span data-stu-id="32ab0-134">See also</span></span>



[<span data-ttu-id="32ab0-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="32ab0-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32ab0-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="32ab0-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32ab0-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="32ab0-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32ab0-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="32ab0-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

