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
# <a name="dtblddlbx"></a><span data-ttu-id="c5985-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="c5985-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="c5985-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5985-105">Описание выпадаемого списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="c5985-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5985-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c5985-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5985-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5985-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="c5985-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c5985-108">Members</span></span>

 <span data-ttu-id="c5985-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c5985-109">**ulFlags**</span></span>
  
> <span data-ttu-id="c5985-110">Зарезервировано, должно быть нуль.</span><span class="sxs-lookup"><span data-stu-id="c5985-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="c5985-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="c5985-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="c5985-112">Тег свойства для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="c5985-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="c5985-113">Это свойство является одним из столбцов в таблице, заданной членом **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="c5985-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="c5985-114">Значения этого свойства отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="c5985-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="c5985-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="c5985-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="c5985-116">Тег свойства для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="c5985-116">Property tag for a property of any type.</span></span> <span data-ttu-id="c5985-117">Это свойство является одним из столбцов в таблице, заданной членом **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="c5985-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="c5985-118">Когда пользователь списка выбирает значение свойства для члена **ulPRDisplayProperty** из строк таблицы, определенной членом **ulPRTableName,** устанавливается соответствующий член **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="c5985-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="c5985-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="c5985-120">Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью вызова **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="c5985-121">Таблица должна иметь два столбца: **ulPRDisplayProperty** и **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="c5985-122">Строки таблицы должны соответствовать пунктам в списке.</span><span class="sxs-lookup"><span data-stu-id="c5985-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5985-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5985-123">Remarks</span></span>

<span data-ttu-id="c5985-124">В **структуре DTBLDDLBX** описывается элемент управления списком в качестве одного элемента, пока пользователь не наберет его.</span><span class="sxs-lookup"><span data-stu-id="c5985-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="c5985-125">Три свойства, которые определены тегами свойств, работают вместе, чтобы отобразить сведения в списке и установить связанное свойство.</span><span class="sxs-lookup"><span data-stu-id="c5985-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="c5985-126">Член **ulPRTableName** — это объект таблицы, к нему можно получить доступ с помощью вызова [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="c5985-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="c5985-127">Таблица имеет два столбца: один столбец для свойства, определенного членом **ulPRDisplayProperty,** а другой для свойства, определенного членом **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="c5985-128">Свойство **ulPRDisplayProperty** является диском для отображения списка.</span><span class="sxs-lookup"><span data-stu-id="c5985-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="c5985-129">Когда пользователь выбирает одно из значений на экране, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить соответствующее свойство, определенное членом **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="c5985-130">Это означает, что свойство в той же строке, что и выбранное свойство отображения.</span><span class="sxs-lookup"><span data-stu-id="c5985-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="c5985-131">Для **члена ulPRSetProperty** нельзя установить PR_NULL **(** [PidTagNull).](pidtagnull-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c5985-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="c5985-132">Начальное значение отображается в списке, если MAPI извлек свойство, представленное членом **ulPRSetProperty,** с помощью вызова [IMAPIProp::GetProps](imapiprop-getprops.md) и расположена строка в таблице со значением для члена **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c5985-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="c5985-133">Начальное отображаемого значения — это содержимое столбца **ulPRDisplayProperty** из этой строки, которое соответствует свойству в члене **ulPRDisplayProperty** структуры.</span><span class="sxs-lookup"><span data-stu-id="c5985-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="c5985-134">Значение, возвращаемого **GetProps** для свойства, определенного членом **ulPRDisplayProperty,** становится начальным значением, которое отображается при первом отображении списка.</span><span class="sxs-lookup"><span data-stu-id="c5985-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="c5985-135">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="c5985-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c5985-136">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="c5985-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="c5985-137">Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c5985-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5985-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c5985-138">See also</span></span>



[<span data-ttu-id="c5985-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c5985-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="c5985-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c5985-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c5985-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="c5985-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="c5985-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c5985-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="c5985-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c5985-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="c5985-144">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="c5985-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="c5985-145">Таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="c5985-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="c5985-146">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="c5985-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

