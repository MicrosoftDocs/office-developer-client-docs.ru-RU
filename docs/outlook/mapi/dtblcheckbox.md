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
# <a name="dtblcheckbox"></a><span data-ttu-id="16d9e-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="16d9e-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="16d9e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16d9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16d9e-105">Содержит сведения о поле, которое будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="16d9e-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16d9e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="16d9e-106">Header file:</span></span>  <br/> |<span data-ttu-id="16d9e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16d9e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="16d9e-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="16d9e-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="16d9e-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="16d9e-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="16d9e-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="16d9e-110">Members</span></span>

 <span data-ttu-id="16d9e-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="16d9e-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="16d9e-112">Положение в памяти строки символов, отображаемой с помощью этого контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="16d9e-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="16d9e-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="16d9e-113">**ulFlags**</span></span>
  
> <span data-ttu-id="16d9e-114">Битовая метка флагов, используемая для обозначения формата метки флажка.</span><span class="sxs-lookup"><span data-stu-id="16d9e-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="16d9e-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="16d9e-115">The following flag can be set:</span></span>
    
<span data-ttu-id="16d9e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16d9e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="16d9e-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="16d9e-117">The label is in Unicode format.</span></span> <span data-ttu-id="16d9e-118">Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="16d9e-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="16d9e-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="16d9e-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="16d9e-120">Тег свойства для свойства типа PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="16d9e-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="16d9e-121">На значение этого свойства влияет состояние этого контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="16d9e-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16d9e-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="16d9e-122">Remarks</span></span>

<span data-ttu-id="16d9e-123">В **структуре DTBLCHECKBOX** описаны контрольные очки, отражающие одно из двух состояния: включено (включено (поле) или отключено (пустое поле).</span><span class="sxs-lookup"><span data-stu-id="16d9e-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="16d9e-124">Член **ulPRPropertyName** описывает boolean свойство, значение которого изменяется путем изменения состояния этого контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="16d9e-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="16d9e-125">При первом отображению этого окна MAPI вызывает метод **GetProps** реализации **IMAPIProp,** связанный с таблицей отображения, для получения набора свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16d9e-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="16d9e-126">Если одно из свойств сопомечается с тегом свойства в структуре **DTBLCHECKBOX,** значение этого свойства отображается в качестве начального значения для этого значения.</span><span class="sxs-lookup"><span data-stu-id="16d9e-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="16d9e-127">Элементы управления для этого можно модификировать.</span><span class="sxs-lookup"><span data-stu-id="16d9e-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="16d9e-128">Это позволяет пользователю изменять свое состояния.</span><span class="sxs-lookup"><span data-stu-id="16d9e-128">This allows a user to change their states.</span></span> <span data-ttu-id="16d9e-129">Модификируемые флажки устанавливают флаг DT_EDITABLE в члене **ulCtlFlags** их [структуры DTCTL](dtctl.md) и в свойстве **PR_CONTROL_FLAGS** ([PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="16d9e-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="16d9e-130">Когда состояние установленного в этом поле изменяется, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить для свойства, обнаруженного в члене тега свойства структуры **DTBLCHECKBOX,** новое состояние.</span><span class="sxs-lookup"><span data-stu-id="16d9e-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="16d9e-131">Например, поставщик адресной книги может включить в диалоговое окно конфигурации изменимый контрольный список, чтобы настроить параметр свойства PR_SEND_RICH_INFO **получателя** ([PidTagSendRichInfo).](pidtagsendrichinfo-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="16d9e-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="16d9e-132">Когда пользователь устанавливает этот контроль, MAPI устанавливает для этого свойства true.</span><span class="sxs-lookup"><span data-stu-id="16d9e-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="16d9e-133">Если этот установлен, для свойства устанавливается false.</span><span class="sxs-lookup"><span data-stu-id="16d9e-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="16d9e-134">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="16d9e-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="16d9e-135">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="16d9e-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="16d9e-136">Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="16d9e-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16d9e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="16d9e-137">See also</span></span>



[<span data-ttu-id="16d9e-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="16d9e-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="16d9e-139">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="16d9e-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="16d9e-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="16d9e-140">MAPI Structures</span></span>](mapi-structures.md)

