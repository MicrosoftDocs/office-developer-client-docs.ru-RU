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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340105"
---
# <a name="dtblddlbx"></a><span data-ttu-id="f2d5e-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="f2d5e-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="f2d5e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2d5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2d5e-105">Описывает раскрывающийся список элементов управления, который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d5e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f2d5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2d5e-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f2d5e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="f2d5e-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f2d5e-108">Members</span></span>

 <span data-ttu-id="f2d5e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f2d5e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="f2d5e-110">ЗаРезервировано, должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="f2d5e-111">**Улпрдисплайпроперти**</span><span class="sxs-lookup"><span data-stu-id="f2d5e-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="f2d5e-112">Тег свойства для свойства типа ПТ_ТСТРИНГ.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="f2d5e-113">Это свойство является одним из столбцов таблицы, определяемой элементом **улпртабленаме** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="f2d5e-114">Значения для этого свойства отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="f2d5e-115">**Улпрсетпроперти**</span><span class="sxs-lookup"><span data-stu-id="f2d5e-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="f2d5e-116">Тег Property для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-116">Property tag for a property of any type.</span></span> <span data-ttu-id="f2d5e-117">Это свойство является одним из столбцов таблицы, определяемой элементом **улпртабленаме** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="f2d5e-118">Когда пользователь списка выбирает значение свойства для элемента **улпрдисплайпроперти** из строк таблицы, определенной элементом **улпртабленаме** , устанавливается соответствующий элемент **улпрсетпроперти** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="f2d5e-119">**Улпртабленаме**</span><span class="sxs-lookup"><span data-stu-id="f2d5e-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="f2d5e-120">Тег свойства для свойства Table типа ПТ_ОБЖЕКТ, которое можно открыть с помощью вызова **опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="f2d5e-121">В таблице должны быть два столбца: **улпрдисплайпроперти** и **улпрсетпроперти**.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="f2d5e-122">Строки таблицы должны соответствовать элементам списка.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2d5e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2d5e-123">Remarks</span></span>

<span data-ttu-id="f2d5e-124">Структура **дтблддлбкс** описывает раскрывающийся список, который отображается в виде одного элемента до тех пор, пока пользователь не выйдет за его развертывание.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="f2d5e-125">Три свойства, определяемые тегами свойства, работают вместе для отображения информации в списке и задания соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="f2d5e-126">Член **улпртабленаме** — это объект Table, доступ к которому осуществляется с помощью вызова [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5e-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="f2d5e-127">В таблице есть два столбца: один столбец для свойства, идентифицируемого элементом **улпрдисплайпроперти** , а другой — для свойства, идентифицируемого элементом **улпрсетпроперти** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="f2d5e-128">Свойство **улпрдисплайпроперти** управляет отображением списка.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="f2d5e-129">Когда пользователь выбирает одно из значений на экране, MAPI вызывает [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать соответствующее свойство, определяемое элементом **улпрсетпроперти** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="f2d5e-130">Это означает, что свойство в той же строке, что и выбранное свойство отображения.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="f2d5e-131">Элемент **улпрсетпроперти** не может иметь значение **пр_нулл** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f2d5e-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="f2d5e-132">Начальное значение отображается в списке, если MAPI получил свойство, представленное элементом **улпрсетпроперти** , через вызов [IMAPIProp::](imapiprop-getprops.md) -PROPS и располагает строку в таблице со значением элемента **улпрсетпроперти** .</span><span class="sxs-lookup"><span data-stu-id="f2d5e-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="f2d5e-133">Начальное отображаемое значение — это содержимое столбца **улпрдисплайпроперти** из этой строки, которое соответствует свойству в элементе **улпрдисплайпроперти** структуры.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="f2d5e-134">Значение, возвращаемое \*\*\*\* свойствами PROPS для свойства, идентифицируемого элементом **улпрдисплайпроперти** , становится начальным значением, которое отображается при первом отображении списка.</span><span class="sxs-lookup"><span data-stu-id="f2d5e-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="f2d5e-135">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5e-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f2d5e-136">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5e-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="f2d5e-137">Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2d5e-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2d5e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="f2d5e-138">See also</span></span>



[<span data-ttu-id="f2d5e-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f2d5e-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="f2d5e-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f2d5e-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f2d5e-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="f2d5e-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="f2d5e-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f2d5e-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="f2d5e-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f2d5e-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="f2d5e-144">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="f2d5e-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="f2d5e-145">Таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="f2d5e-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="f2d5e-146">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="f2d5e-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

