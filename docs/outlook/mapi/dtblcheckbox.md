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
# <a name="dtblcheckbox"></a><span data-ttu-id="50e98-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="50e98-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="50e98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50e98-105">Содержит сведения о поле, которое будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="50e98-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50e98-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="50e98-106">Header file:</span></span>  <br/> |<span data-ttu-id="50e98-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50e98-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="50e98-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="50e98-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="50e98-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="50e98-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="50e98-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="50e98-110">Members</span></span>

 <span data-ttu-id="50e98-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="50e98-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="50e98-112">Положение в памяти строки символов, отображаемой с помощью контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="50e98-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="50e98-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="50e98-113">**ulFlags**</span></span>
  
> <span data-ttu-id="50e98-114">Bitmask флагов, используемых для обозначения формата метки флажка.</span><span class="sxs-lookup"><span data-stu-id="50e98-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="50e98-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="50e98-115">The following flag can be set:</span></span>
    
<span data-ttu-id="50e98-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50e98-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50e98-117">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="50e98-117">The label is in Unicode format.</span></span> <span data-ttu-id="50e98-118">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="50e98-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="50e98-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="50e98-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="50e98-120">Тег свойства для свойства типа PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="50e98-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="50e98-121">На значение этого свойства влияет состояние контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="50e98-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50e98-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="50e98-122">Remarks</span></span>

<span data-ttu-id="50e98-123">Структура **DTBLCHECKBOX** описывает контрольное окно, которое отражает одно из двух штатов: включено (контрольное поле) или отключено (пустое поле).</span><span class="sxs-lookup"><span data-stu-id="50e98-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="50e98-124">Участник **ulPRPropertyName** описывает свойство Boolean, значение которого управляется изменением состояния контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="50e98-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="50e98-125">При первом отображке контрольного окна MAPI вызывает метод **GetProps** реализации **IMAPIProp,** связанный со таблицей отображения, чтобы получить набор свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50e98-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="50e98-126">Если одно из свойств отображает тег свойства в структуре **DTBLCHECKBOX,** значение для этого свойства отображается в качестве начального значения контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="50e98-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="50e98-127">Элементы управления контрольными окнами можно модификировать.</span><span class="sxs-lookup"><span data-stu-id="50e98-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="50e98-128">Это позволяет пользователю изменять свои состояния.</span><span class="sxs-lookup"><span data-stu-id="50e98-128">This allows a user to change their states.</span></span> <span data-ttu-id="50e98-129">Флажки модификата устанавливают флаг DT_EDITABLE в **члене ulCtlFlags** их [структуры DTCTL](dtctl.md) **и** в свойстве [PR_CONTROL_FLAGS (PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="50e98-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="50e98-130">При изменениях состояния почтового ящика MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить свойство, идентифицированное в члене тега свойств структуры **DTBLCHECKBOX,** в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="50e98-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="50e98-131">Например, поставщик адресных книг может включить в диалоговое окно конфигурации управление изменяемым контрольным окном для настройки параметра свойства[PR_SEND_RICH_INFO (PidTagSendRichInfo).](pidtagsendrichinfo-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="50e98-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="50e98-132">Когда пользователь выбирает контрольный ящик, MAPI задает это свойство true.</span><span class="sxs-lookup"><span data-stu-id="50e98-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="50e98-133">При отсеклении контрольного окна свойство настроено на FALSE.</span><span class="sxs-lookup"><span data-stu-id="50e98-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="50e98-134">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="50e98-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="50e98-135">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="50e98-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="50e98-136">Сведения о типах свойств см. в [обзоре типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="50e98-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50e98-137">См. также</span><span class="sxs-lookup"><span data-stu-id="50e98-137">See also</span></span>



[<span data-ttu-id="50e98-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="50e98-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="50e98-139">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="50e98-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="50e98-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="50e98-140">MAPI Structures</span></span>](mapi-structures.md)

