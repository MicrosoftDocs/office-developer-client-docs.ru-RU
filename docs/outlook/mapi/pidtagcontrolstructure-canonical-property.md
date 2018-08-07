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
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811006"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="074ac-103">Каноническое свойство PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="074ac-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="074ac-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="074ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="074ac-105">Содержит указатель на структуру для элемента управления, используемый в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="074ac-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="074ac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="074ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="074ac-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="074ac-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="074ac-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="074ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="074ac-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="074ac-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="074ac-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="074ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="074ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="074ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="074ac-112">Область:</span><span class="sxs-lookup"><span data-stu-id="074ac-112">Area:</span></span>  <br/> |<span data-ttu-id="074ac-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="074ac-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="074ac-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="074ac-114">Remarks</span></span>

<span data-ttu-id="074ac-115">Это свойство представляет длинный указатель, привести к одному из структуры элемента управления.</span><span class="sxs-lookup"><span data-stu-id="074ac-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="074ac-116">Управляющие структуры относятся:</span><span class="sxs-lookup"><span data-stu-id="074ac-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="074ac-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="074ac-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="074ac-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="074ac-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="074ac-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="074ac-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="074ac-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="074ac-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="074ac-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="074ac-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="074ac-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="074ac-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="074ac-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="074ac-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="074ac-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="074ac-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="074ac-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="074ac-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="074ac-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="074ac-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="074ac-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="074ac-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="074ac-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="074ac-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="074ac-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="074ac-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="074ac-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="074ac-130">Header files</span></span>

<span data-ttu-id="074ac-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="074ac-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="074ac-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="074ac-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="074ac-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="074ac-133">Mapitags.h</span></span>
  
> <span data-ttu-id="074ac-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="074ac-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="074ac-135">См. также</span><span class="sxs-lookup"><span data-stu-id="074ac-135">See also</span></span>



[<span data-ttu-id="074ac-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="074ac-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="074ac-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="074ac-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="074ac-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="074ac-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="074ac-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="074ac-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

