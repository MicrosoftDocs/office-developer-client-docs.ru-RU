---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438570"
---
# <a name="dtbllbx"></a><span data-ttu-id="5f787-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="5f787-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="5f787-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f787-105">Описывает список, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="5f787-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f787-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5f787-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f787-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f787-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="5f787-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5f787-108">Members</span></span>

 <span data-ttu-id="5f787-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5f787-109">**ulFlags**</span></span>
  
> <span data-ttu-id="5f787-110">Битоваяmas флагов, используемая для устранения горизонтальной или вертикальной полоса прокрутки в списке.</span><span class="sxs-lookup"><span data-stu-id="5f787-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="5f787-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5f787-111">The following flags can be set:</span></span>
    
<span data-ttu-id="5f787-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="5f787-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="5f787-113">Горизонтальная полоса прокрутки не должна быть показана вместе со списком.</span><span class="sxs-lookup"><span data-stu-id="5f787-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="5f787-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="5f787-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="5f787-115">Вертикальная лямка прокрутки не должна быть показана вместе со списком.</span><span class="sxs-lookup"><span data-stu-id="5f787-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="5f787-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="5f787-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="5f787-117">Тег свойства для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="5f787-117">Property tag for a property of any type.</span></span> <span data-ttu-id="5f787-118">Это свойство является одним из столбцов в таблице, заданной членом **ulPRTableTable.**</span><span class="sxs-lookup"><span data-stu-id="5f787-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="5f787-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="5f787-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="5f787-120">Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью вызова **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="5f787-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="5f787-121">Число столбцов в таблице зависит от того, является ли список одним или нескольким списком выбора.</span><span class="sxs-lookup"><span data-stu-id="5f787-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="5f787-122">Если для **члена ulPRSetProperty** установлено PR_NULL **(** [PidTagNull),](pidtagnull-canonical-property.md)список позволяет выбрать несколько вариантов.</span><span class="sxs-lookup"><span data-stu-id="5f787-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f787-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f787-123">Remarks</span></span>

<span data-ttu-id="5f787-124">Структура **DTBLLBX** описывает список элементов управления, используемых для показа нескольких элементов и позволяя пользователю выбрать один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="5f787-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="5f787-125">Члены **ulPRSetProperty** и **ulPRTableName** работают вместе; Если в таблице выбрано одно значение, оно возвращается в **ulPRSetProperty,** когда диалоговое окно будет отклонено.</span><span class="sxs-lookup"><span data-stu-id="5f787-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="5f787-126">Значение флагов указывает, должна ли отображаться горизонтальная или вертикальная полоса прокрутки со списком.</span><span class="sxs-lookup"><span data-stu-id="5f787-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="5f787-127">По умолчанию типы полос прокрутки отображаются, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5f787-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="5f787-128">Поставщики услуг могут настроить MAPI_NO_HBAR подавления горизонтальной полоса прокрутки и MAPI_NO_VBAR для подавления вертикальной полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="5f787-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="5f787-129">Два элемента тега свойства совместно отображают значения в списке и устанавливают соответствующие свойства при выборе элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="5f787-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="5f787-130">При первом отображении списка MAPI вызывает метод **OpenProperty** реализации **IMAPIProp** для получения таблицы, определенной в члене **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="5f787-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="5f787-131">Количество столбцов в таблице зависит от значения члена **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="5f787-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="5f787-132">Если **для ulPRSetProperty** установлено **PR_NULL,** список является списком выбора нескольких объектов, основанных на объекте, который содержит получателей, таких как контейнер адресной книги, таблица получателей для сообщения или таблица содержимого списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="5f787-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="5f787-133">Таблица для нескольких списков выбора должна включать следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="5f787-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="5f787-134">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5f787-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="5f787-135">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5f787-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="5f787-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5f787-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="5f787-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)и не более пяти других многоценных свойств строки также могут отображаться с тремя требуми столбцами.</span><span class="sxs-lookup"><span data-stu-id="5f787-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="5f787-138">Если для **члена ulPRSetProperty** не установлено **PR_NULL,** список является одним списком выбора.</span><span class="sxs-lookup"><span data-stu-id="5f787-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="5f787-139">Начальное значение **ulPRSetProperty** определяет первую выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5f787-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="5f787-140">Когда пользователь выбирает одну из строк, для члена **ulPRSetProperty** устанавливается выбранное значение, и это значение записуется обратно в реализацию интерфейса свойства с вызовом [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="5f787-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="5f787-141">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5f787-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="5f787-142">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="5f787-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f787-143">См. также</span><span class="sxs-lookup"><span data-stu-id="5f787-143">See also</span></span>



[<span data-ttu-id="5f787-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="5f787-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="5f787-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5f787-145">MAPI Structures</span></span>](mapi-structures.md)

