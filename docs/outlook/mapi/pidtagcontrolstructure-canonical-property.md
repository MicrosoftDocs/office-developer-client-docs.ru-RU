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
ms.openlocfilehash: 3b517888d562ee5b178dbd011fa1ce6ab218c6b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594357"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="9ba5f-103">Каноническое свойство PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="9ba5f-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="9ba5f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ba5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ba5f-105">Содержит указатель на структуру для элемента управления, используемый в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba5f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9ba5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ba5f-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="9ba5f-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="9ba5f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9ba5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ba5f-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="9ba5f-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="9ba5f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ba5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ba5f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ba5f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ba5f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9ba5f-112">Area:</span></span>  <br/> |<span data-ttu-id="9ba5f-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="9ba5f-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba5f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ba5f-114">Remarks</span></span>

<span data-ttu-id="9ba5f-115">Это свойство представляет длинный указатель, привести к одному из структуры элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="9ba5f-116">Управляющие структуры относятся:</span><span class="sxs-lookup"><span data-stu-id="9ba5f-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="9ba5f-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="9ba5f-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="9ba5f-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="9ba5f-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="9ba5f-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="9ba5f-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="9ba5f-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="9ba5f-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="9ba5f-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="9ba5f-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="9ba5f-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="9ba5f-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="9ba5f-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="9ba5f-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="9ba5f-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="9ba5f-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="9ba5f-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="9ba5f-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9ba5f-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ba5f-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ba5f-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ba5f-130">Header files</span></span>

<span data-ttu-id="9ba5f-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ba5f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ba5f-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ba5f-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ba5f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9ba5f-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ba5f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9ba5f-135">See also</span></span>



[<span data-ttu-id="9ba5f-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ba5f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ba5f-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ba5f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ba5f-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ba5f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ba5f-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ba5f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

