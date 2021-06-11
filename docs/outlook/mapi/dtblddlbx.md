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
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438850"
---
# <a name="dtblddlbx"></a><span data-ttu-id="22778-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="22778-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="22778-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22778-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22778-105">Описывает выпадаемую таблицу управления списком, которая будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="22778-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22778-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="22778-106">Header file:</span></span>  <br/> |<span data-ttu-id="22778-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22778-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="22778-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="22778-108">Members</span></span>

 <span data-ttu-id="22778-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="22778-109">**ulFlags**</span></span>
  
> <span data-ttu-id="22778-110">Зарезервировано, должно быть ноль.</span><span class="sxs-lookup"><span data-stu-id="22778-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="22778-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="22778-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="22778-112">Тег свойства для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="22778-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="22778-113">Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="22778-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="22778-114">Значения этого свойства отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="22778-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="22778-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="22778-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="22778-116">Тег свойства для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="22778-116">Property tag for a property of any type.</span></span> <span data-ttu-id="22778-117">Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="22778-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="22778-118">Когда пользователь списка выбирает значение свойства для члена **ulPRDisplayProperty** из строк таблицы, идентифицированных участником **ulPRTableName,** устанавливается соответствующий член **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="22778-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="22778-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="22778-120">Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью **вызова OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="22778-121">В таблице должно быть два столбца: **ulPRDisplayProperty** и **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="22778-122">Строки таблицы должны соответствовать пунктам в списке.</span><span class="sxs-lookup"><span data-stu-id="22778-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22778-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="22778-123">Remarks</span></span>

<span data-ttu-id="22778-124">Структура **DTBLDDLBX** описывает элемент управления списком, отображаемый как единый элемент до тех пор, пока пользователь не выберет решение о его расширении.</span><span class="sxs-lookup"><span data-stu-id="22778-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="22778-125">Три свойства, идентифицированные тегами свойств, работают вместе, чтобы отобразить сведения в списке и установить связанное свойство.</span><span class="sxs-lookup"><span data-stu-id="22778-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="22778-126">Член **ulPRTableName** — это объект таблицы, к нему можно получить доступ по вызову [в IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="22778-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="22778-127">В таблице есть два столбца: один столбец для свойства, определенного участником **ulPRDisplayProperty,** а другой для свойства, определенного участником **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="22778-128">Свойство **ulPRDisplayProperty** диски отображения списка.</span><span class="sxs-lookup"><span data-stu-id="22778-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="22778-129">Когда пользователь выбирает одно из значений из дисплея, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить соответствующее свойство, определенное участником **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="22778-130">Это означает, что свойство в одной строке с выбранным свойством отображения.</span><span class="sxs-lookup"><span data-stu-id="22778-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="22778-131">Нельзя установить для участника **ulPRSetProperty** **PR_NULL** [(PidTagNull).](pidtagnull-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="22778-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="22778-132">Начальное значение отображается в списке, если MAPI извлекла свойство, представленное участником **ulPRSetProperty,** с помощью вызова [в IMAPIProp::GetProps](imapiprop-getprops.md) и расположена строка в таблице со значением для члена **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="22778-133">Начальное отображаемого значения — содержимое столбца **ulPRDisplayProperty** из этой строки, которое соответствует свойству в **члене структуры ulPRDisplayProperty.**</span><span class="sxs-lookup"><span data-stu-id="22778-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="22778-134">Значение, возвращенное **GetProps** для свойства, определенного участником **ulPRDisplayProperty,** становится начальным значением, которое отображается при первом отображении списка.</span><span class="sxs-lookup"><span data-stu-id="22778-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="22778-135">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="22778-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="22778-136">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="22778-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="22778-137">Сведения о типах свойств см. в [обзоре типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="22778-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22778-138">См. также</span><span class="sxs-lookup"><span data-stu-id="22778-138">See also</span></span>



[<span data-ttu-id="22778-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="22778-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="22778-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="22778-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="22778-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="22778-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="22778-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="22778-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="22778-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="22778-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="22778-144">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="22778-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="22778-145">Таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="22778-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="22778-146">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="22778-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

