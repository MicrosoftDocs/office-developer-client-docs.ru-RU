---
title: Каноническое свойство PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf91620042f916d51f27be50d15f72db537ad5f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412949"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="5517b-103">Каноническое свойство PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="5517b-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="5517b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5517b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5517b-105">Содержит указатель на структуру для управления, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5517b-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5517b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5517b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5517b-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="5517b-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="5517b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5517b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5517b-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="5517b-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="5517b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5517b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5517b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5517b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5517b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5517b-112">Area:</span></span>  <br/> |<span data-ttu-id="5517b-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="5517b-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5517b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5517b-114">Remarks</span></span>

<span data-ttu-id="5517b-115">Это свойство представляет собой длинную указатель, отбрасываемую в одну из структур управления.</span><span class="sxs-lookup"><span data-stu-id="5517b-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="5517b-116">Структуры управления включают:</span><span class="sxs-lookup"><span data-stu-id="5517b-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="5517b-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="5517b-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="5517b-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="5517b-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="5517b-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="5517b-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="5517b-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="5517b-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="5517b-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="5517b-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="5517b-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="5517b-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="5517b-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="5517b-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="5517b-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="5517b-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="5517b-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="5517b-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="5517b-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="5517b-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="5517b-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5517b-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="5517b-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="5517b-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5517b-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5517b-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5517b-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5517b-130">Header files</span></span>

<span data-ttu-id="5517b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5517b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5517b-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5517b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5517b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5517b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5517b-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5517b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5517b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5517b-135">See also</span></span>



[<span data-ttu-id="5517b-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5517b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5517b-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5517b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5517b-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5517b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5517b-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5517b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

