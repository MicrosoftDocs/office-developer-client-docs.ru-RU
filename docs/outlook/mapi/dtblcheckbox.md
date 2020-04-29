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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436834"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="36580-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="36580-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="36580-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36580-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36580-105">Содержит сведения об установленном флажке, который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="36580-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36580-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="36580-106">Header file:</span></span>  <br/> |<span data-ttu-id="36580-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="36580-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="36580-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="36580-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="36580-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="36580-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="36580-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="36580-110">Members</span></span>

 <span data-ttu-id="36580-111">**улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="36580-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="36580-112">Позиция в памяти строки символов, которая отображается вместе с флажком.</span><span class="sxs-lookup"><span data-stu-id="36580-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="36580-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="36580-113">**ulFlags**</span></span>
  
> <span data-ttu-id="36580-114">Битовая маска флагов, используемых для обозначения формата метки флажка.</span><span class="sxs-lookup"><span data-stu-id="36580-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="36580-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="36580-115">The following flag can be set:</span></span>
    
<span data-ttu-id="36580-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36580-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36580-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="36580-117">The label is in Unicode format.</span></span> <span data-ttu-id="36580-118">Если флаг MAPI_UNICODE не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="36580-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="36580-119">**улпрпропертинаме**</span><span class="sxs-lookup"><span data-stu-id="36580-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="36580-120">Тег свойства для свойства типа PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="36580-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="36580-121">Значение этого свойства зависит от состояния флажка.</span><span class="sxs-lookup"><span data-stu-id="36580-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36580-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="36580-122">Remarks</span></span>

<span data-ttu-id="36580-123">Структура **дтблчеккбокс** описывает флажок элемента управления, который отражает одно из двух состояний: включено (отмечено флажком) или Disabled (пустое поле).</span><span class="sxs-lookup"><span data-stu-id="36580-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="36580-124">Элемент **улпрпропертинаме** описывает свойство Boolean, значение которого изменяется при изменении состояния флажка.</span><span class="sxs-lookup"><span data-stu-id="36580-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="36580-125">При первом отображении этого флажка MAPI вызывает метод **PROPS** реализации **IMAPIProp** , связанной с таблицей отображения, для получения набора свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36580-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="36580-126">Если одно из свойств сопоставлено с тегом свойства в структуре **дтблчеккбокс** , значение этого свойства отображается в качестве начального значения флажка.</span><span class="sxs-lookup"><span data-stu-id="36580-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="36580-127">Элементы управления "флажок" могут быть изменяемыми.</span><span class="sxs-lookup"><span data-stu-id="36580-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="36580-128">Это позволяет пользователю изменять свои состояния.</span><span class="sxs-lookup"><span data-stu-id="36580-128">This allows a user to change their states.</span></span> <span data-ttu-id="36580-129">Изменяемые флажки установите флаг DT_EDITABLE в элементе **улктлфлагс** структуры [дтктл](dtctl.md) и в их свойстве **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="36580-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="36580-130">Когда флажок изменит свое состояние, MAPI вызывает [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать свойство, указанное в элементе тега свойства в структуре **дтблчеккбокс** , в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="36580-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="36580-131">Например, поставщик адресной книги может содержать изменяемый элемент управления "флажок" в диалоговом окне настройки, чтобы настроить значение свойства **PR_SEND_RICH_INFO** получателя ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="36580-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="36580-132">Когда пользователь устанавливает этот флажок, MAPI устанавливает для этого свойства значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="36580-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="36580-133">Если этот флажок не установлен, свойству присваивается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="36580-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="36580-134">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="36580-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="36580-135">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="36580-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="36580-136">Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36580-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36580-137">См. также</span><span class="sxs-lookup"><span data-stu-id="36580-137">See also</span></span>



[<span data-ttu-id="36580-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="36580-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="36580-139">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="36580-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="36580-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="36580-140">MAPI Structures</span></span>](mapi-structures.md)

