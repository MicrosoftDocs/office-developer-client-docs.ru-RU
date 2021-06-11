---
title: Каноническое свойство PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734205"
---
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="064c7-103">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="064c7-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="064c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="064c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="064c7-105">Содержит значение, указывающее тип управления для управления, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="064c7-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="064c7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="064c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="064c7-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="064c7-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="064c7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="064c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="064c7-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="064c7-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="064c7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="064c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="064c7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="064c7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="064c7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="064c7-112">Area:</span></span>  <br/> |<span data-ttu-id="064c7-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="064c7-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="064c7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="064c7-114">Remarks</span></span>

<span data-ttu-id="064c7-115">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="064c7-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="064c7-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="064c7-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="064c7-117">Метка диалогов.</span><span class="sxs-lookup"><span data-stu-id="064c7-117">A dialog label.</span></span>
   
<span data-ttu-id="064c7-118">DTCT_EDIT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="064c7-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="064c7-119">Диалоговое окно для редактирования текста.</span><span class="sxs-lookup"><span data-stu-id="064c7-119">A dialog edit text box.</span></span>

<span data-ttu-id="064c7-120">DTCT_LBX (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="064c7-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="064c7-121">Диалоговое поле списка.</span><span class="sxs-lookup"><span data-stu-id="064c7-121">A dialog list box.</span></span>
    
<span data-ttu-id="064c7-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="064c7-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="064c7-123">Диалоговое комбо поле.</span><span class="sxs-lookup"><span data-stu-id="064c7-123">A dialog combo box.</span></span>

<span data-ttu-id="064c7-124">DTCT_DDLBX (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="064c7-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="064c7-125">Диалоговое окно списка.</span><span class="sxs-lookup"><span data-stu-id="064c7-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="064c7-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="064c7-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="064c7-127">Диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="064c7-127">A dialog check box.</span></span>

<span data-ttu-id="064c7-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="064c7-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="064c7-129">Диалоговое групповое окно.</span><span class="sxs-lookup"><span data-stu-id="064c7-129">A dialog group box.</span></span>
  
<span data-ttu-id="064c7-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="064c7-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="064c7-131">Управление кнопкой диалогов.</span><span class="sxs-lookup"><span data-stu-id="064c7-131">A dialog button control.</span></span>
    
<span data-ttu-id="064c7-132">DTCT_PAGE (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="064c7-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="064c7-133">Страница на вкладке диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="064c7-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="064c7-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="064c7-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="064c7-135">Кнопка радио диалогов.</span><span class="sxs-lookup"><span data-stu-id="064c7-135">A dialog radio button.</span></span>
    
<span data-ttu-id="064c7-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="064c7-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="064c7-137">Многоценное поле списка, заполненное многоценным свойством строки типа.</span><span class="sxs-lookup"><span data-stu-id="064c7-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="064c7-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="064c7-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="064c7-139">Многооценное поле списка,заполненное многоценным свойством строки типа.</span><span class="sxs-lookup"><span data-stu-id="064c7-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="064c7-140">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="064c7-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="064c7-141">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="064c7-141">Header files</span></span>

<span data-ttu-id="064c7-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="064c7-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="064c7-143">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="064c7-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="064c7-144">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="064c7-144">mapitags.h</span></span>
  
> <span data-ttu-id="064c7-145">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="064c7-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="064c7-146">См. также</span><span class="sxs-lookup"><span data-stu-id="064c7-146">See also</span></span>



[<span data-ttu-id="064c7-147">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="064c7-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="064c7-148">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="064c7-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="064c7-149">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="064c7-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="064c7-150">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="064c7-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

