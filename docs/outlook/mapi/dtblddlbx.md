---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db95697cd98e66da9fb3d0cd0180b238c0a8dff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808348"
---
# <a name="dtblddlbx"></a><span data-ttu-id="fb068-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="fb068-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="fb068-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb068-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb068-105">Описывает элемент управления раскрывающегося списка, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="fb068-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb068-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fb068-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb068-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb068-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="fb068-108">Members</span><span class="sxs-lookup"><span data-stu-id="fb068-108">Members</span></span>

 <span data-ttu-id="fb068-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fb068-109">**ulFlags**</span></span>
  
> <span data-ttu-id="fb068-110">Зарезервированные, должен быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fb068-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="fb068-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="fb068-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="fb068-112">Свойство tag для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="fb068-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="fb068-113">Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="fb068-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="fb068-114">Значения для этого свойства отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="fb068-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="fb068-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="fb068-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="fb068-116">Свойство tag для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="fb068-116">Property tag for a property of any type.</span></span> <span data-ttu-id="fb068-117">Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="fb068-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="fb068-118">Когда пользователь списка выбирает значение свойства для элемента **ulPRDisplayProperty** из строки в таблице, определяемую средством член **ulPRTableName** , соответствующего члена **ulPRSetProperty** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="fb068-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="fb068-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="fb068-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="fb068-120">Тег свойства для свойства в таблице типа PT_OBJECT, которая может быть открыта с помощью **OpenProperty** вызова.</span><span class="sxs-lookup"><span data-stu-id="fb068-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="fb068-121">Таблица должна иметь два столбца: **ulPRDisplayProperty** и **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="fb068-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="fb068-122">Строки в таблице должна соответствовать элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="fb068-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb068-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb068-123">Remarks</span></span>

<span data-ttu-id="fb068-124">Структура **DTBLDDLBX** описывает элемент управления раскрывающегося списка, который отображается в виде одного элемента, пока пользователь вручную развернуть его.</span><span class="sxs-lookup"><span data-stu-id="fb068-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="fb068-125">Три свойства, определяемую средством теги свойства работают вместе для отображения сведений в списке и связанных с ними свойства.</span><span class="sxs-lookup"><span data-stu-id="fb068-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="fb068-126">Член **ulPRTableName** — это объект таблицы, к которому осуществляется посредством вызова [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="fb068-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="fb068-127">Таблица имеет два столбца: один столбец для свойства, определяемую средством член **ulPRDisplayProperty** , а другой для свойство, определяемое член **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="fb068-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="fb068-128">Свойство **ulPRDisplayProperty** дисков Отображение списка.</span><span class="sxs-lookup"><span data-stu-id="fb068-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="fb068-129">Когда пользователь выбирает одно из значений из отображения, MAPI вызывает [IMAPIProp::SetProps](imapiprop-setprops.md) для соответствующего свойства согласно процедуре участником **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="fb068-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="fb068-130">Это означает, что свойство в той же строке выбранного отображаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="fb068-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="fb068-131">Член **ulPRSetProperty** не может иметь значение **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fb068-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="fb068-132">Начальное значение отображается в списке, если MAPI имеет извлекается свойство, представленное член **ulPRSetProperty** посредством вызова [IMAPIProp::GetProps](imapiprop-getprops.md) и находится строки в таблице со значением для элемента **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="fb068-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="fb068-133">Начальное отображаемое значение находится содержимое столбца **ulPRDisplayProperty** из этой строки, соответствующее свойство в элемент **ulPRDisplayProperty** структуры.</span><span class="sxs-lookup"><span data-stu-id="fb068-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="fb068-134">Значение, возвращаемое **GetProps** для свойства, определяемую средством член **ulPRDisplayProperty** становится начального значения, которая отображается при первом отображении списка.</span><span class="sxs-lookup"><span data-stu-id="fb068-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="fb068-135">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fb068-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="fb068-136">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="fb068-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="fb068-137">Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb068-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb068-138">См. также</span><span class="sxs-lookup"><span data-stu-id="fb068-138">See also</span></span>



[<span data-ttu-id="fb068-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="fb068-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="fb068-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="fb068-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="fb068-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="fb068-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="fb068-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="fb068-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="fb068-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="fb068-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="fb068-144">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="fb068-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="fb068-145">Таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="fb068-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="fb068-146">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="fb068-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

