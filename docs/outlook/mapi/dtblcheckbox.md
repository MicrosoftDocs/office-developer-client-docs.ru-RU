---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808341"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="2defa-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="2defa-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="2defa-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2defa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2defa-105">Содержит сведения о флажок, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="2defa-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2defa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2defa-106">Header file:</span></span>  <br/> |<span data-ttu-id="2defa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2defa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2defa-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="2defa-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="2defa-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="2defa-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="2defa-110">Members</span><span class="sxs-lookup"><span data-stu-id="2defa-110">Members</span></span>

 <span data-ttu-id="2defa-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="2defa-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2defa-112">Положение в памяти строку символов, которое будет отображаться с флажок.</span><span class="sxs-lookup"><span data-stu-id="2defa-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="2defa-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2defa-113">**ulFlags**</span></span>
  
> <span data-ttu-id="2defa-114">Битовая маска флаги используется для назначения формат метки.</span><span class="sxs-lookup"><span data-stu-id="2defa-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="2defa-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2defa-115">The following flag can be set:</span></span>
    
<span data-ttu-id="2defa-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2defa-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2defa-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="2defa-117">The label is in Unicode format.</span></span> <span data-ttu-id="2defa-118">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="2defa-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="2defa-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="2defa-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="2defa-120">Свойство tag для свойства типа PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="2defa-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="2defa-121">Значение этого свойства зависит от состояния флажка.</span><span class="sxs-lookup"><span data-stu-id="2defa-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2defa-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="2defa-122">Remarks</span></span>

<span data-ttu-id="2defa-123">Структура **DTBLCHECKBOX** описывает флажок элемент управления, который отражает один из двух режимов: (флажком) включены или отключены (пустые поля).</span><span class="sxs-lookup"><span data-stu-id="2defa-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="2defa-124">Член **ulPRPropertyName** описывает логическое свойство, значение которого управляется изменение состояния флажка.</span><span class="sxs-lookup"><span data-stu-id="2defa-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="2defa-125">При первом отображении флажок MAPI вызывает метод **GetProps** реализации **IMAPIProp** , связанный с таблицей отображения для получения набора свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2defa-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="2defa-126">Если одно из свойств соответствует тег свойства в структуре **DTBLCHECKBOX** , значение для этого свойства отображается в поле проверить начальное значение.</span><span class="sxs-lookup"><span data-stu-id="2defa-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="2defa-127">Элементы управления "флажок" можно изменить.</span><span class="sxs-lookup"><span data-stu-id="2defa-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="2defa-128">Это позволяет пользователю изменять их состояния.</span><span class="sxs-lookup"><span data-stu-id="2defa-128">This allows a user to change their states.</span></span> <span data-ttu-id="2defa-129">Можно изменить флажки установить флаг DT_EDITABLE в **ulCtlFlags** членом их [DTCTL](dtctl.md) структуры и их свойства **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2defa-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="2defa-130">При изменении его состояния флажка MAPI вызывает [IMAPIProp::SetProps](imapiprop-setprops.md) для свойства, определенный в член тега свойства структуры **DTBLCHECKBOX** новое состояние.</span><span class="sxs-lookup"><span data-stu-id="2defa-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="2defa-131">К примеру поставщика адресных книг могут содержать элемент управления можно изменить флажок в диалоговое окно настройки его настроить свойство **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) получателя.</span><span class="sxs-lookup"><span data-stu-id="2defa-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="2defa-132">Когда пользователь выбирает этот флажок, MAPI задает это свойство в значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="2defa-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="2defa-133">Если флажок не выбран, свойство имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="2defa-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="2defa-134">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2defa-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2defa-135">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="2defa-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="2defa-136">Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2defa-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2defa-137">См. также</span><span class="sxs-lookup"><span data-stu-id="2defa-137">See also</span></span>



[<span data-ttu-id="2defa-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2defa-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="2defa-139">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="2defa-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="2defa-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="2defa-140">MAPI Structures</span></span>](mapi-structures.md)

