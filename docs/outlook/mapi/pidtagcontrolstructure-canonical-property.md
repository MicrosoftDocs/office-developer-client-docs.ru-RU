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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335247"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="f6ab9-103">Каноническое свойство PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="f6ab9-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="f6ab9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6ab9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6ab9-105">Содержит указатель на структуру для элемента управления, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6ab9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f6ab9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6ab9-107">ПР_КОНТРОЛ_СТРУКТУРЕ</span><span class="sxs-lookup"><span data-stu-id="f6ab9-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="f6ab9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f6ab9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6ab9-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="f6ab9-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="f6ab9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f6ab9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6ab9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6ab9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6ab9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f6ab9-112">Area:</span></span>  <br/> |<span data-ttu-id="f6ab9-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="f6ab9-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6ab9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6ab9-114">Remarks</span></span>

<span data-ttu-id="f6ab9-115">Это свойство представляет длинный указатель, приведенный к одной из структур управления.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="f6ab9-116">Структуры управления включают:</span><span class="sxs-lookup"><span data-stu-id="f6ab9-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="f6ab9-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="f6ab9-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="f6ab9-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="f6ab9-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="f6ab9-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="f6ab9-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="f6ab9-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="f6ab9-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="f6ab9-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="f6ab9-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="f6ab9-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="f6ab9-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="f6ab9-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="f6ab9-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="f6ab9-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f6ab9-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="f6ab9-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f6ab9-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f6ab9-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f6ab9-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f6ab9-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="f6ab9-130">Header files</span></span>

<span data-ttu-id="f6ab9-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f6ab9-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6ab9-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6ab9-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f6ab9-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f6ab9-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6ab9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f6ab9-135">See also</span></span>



[<span data-ttu-id="f6ab9-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6ab9-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6ab9-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f6ab9-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6ab9-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f6ab9-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6ab9-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f6ab9-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

