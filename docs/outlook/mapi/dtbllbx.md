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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321238"
---
# <a name="dtbllbx"></a><span data-ttu-id="4007a-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="4007a-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="4007a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4007a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4007a-105">Описывает список, который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="4007a-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4007a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4007a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4007a-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4007a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="4007a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="4007a-108">Members</span></span>

 <span data-ttu-id="4007a-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4007a-109">**ulFlags**</span></span>
  
> <span data-ttu-id="4007a-110">Битовая маска флагов, используемая для удаления горизонтальной или вертикальной полосы прокрутки из списка.</span><span class="sxs-lookup"><span data-stu-id="4007a-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="4007a-111">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4007a-111">The following flags can be set:</span></span>
    
<span data-ttu-id="4007a-112">МАПИ_НО_ХБАР</span><span class="sxs-lookup"><span data-stu-id="4007a-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="4007a-113">В списке не должно отображаться горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4007a-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="4007a-114">МАПИ_НО_ВБАР</span><span class="sxs-lookup"><span data-stu-id="4007a-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="4007a-115">В списке не должно отображаться вертикальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4007a-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="4007a-116">**Улпрсетпроперти**</span><span class="sxs-lookup"><span data-stu-id="4007a-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="4007a-117">Тег Property для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="4007a-117">Property tag for a property of any type.</span></span> <span data-ttu-id="4007a-118">Это свойство является одним из столбцов таблицы, определяемой элементом **улпртаблетабле** .</span><span class="sxs-lookup"><span data-stu-id="4007a-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="4007a-119">**Улпртабленаме**</span><span class="sxs-lookup"><span data-stu-id="4007a-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="4007a-120">Тег свойства для свойства Table типа ПТ_ОБЖЕКТ, которое можно открыть с помощью вызова **опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="4007a-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="4007a-121">Количество столбцов, которые должна иметь таблица, зависит от того, является ли список одним или несколькими вариантами выбора.</span><span class="sxs-lookup"><span data-stu-id="4007a-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="4007a-122">Если для члена **улпрсетпроперти** задано значение **пр_нулл** ([PidTagNull](pidtagnull-canonical-property.md)), в списке можно выбрать несколько вариантов.</span><span class="sxs-lookup"><span data-stu-id="4007a-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4007a-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="4007a-123">Remarks</span></span>

<span data-ttu-id="4007a-124">Структура **дтбллбкс** описывает список элементов управления, которые используются для отображения нескольких элементов и позволяют пользователю выбрать один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="4007a-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="4007a-125">Члены **улпрсетпроперти** и **улпртабленаме** работают совместно; когда из таблицы выбирается одно значение, оно записывается обратно в **улпрсетпроперти** при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4007a-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="4007a-126">Значение Flags указывает, должна ли отображаться в списке горизонтальная или вертикальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4007a-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="4007a-127">По умолчанию при необходимости отображаются типы полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4007a-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="4007a-128">Поставщики услуг могут настроить МАПИ_НО_ХБАР для отключения горизонтальной полосы прокрутки и МАПИ_НО_ВБАР для подавления вертикальной полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4007a-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="4007a-129">Два элемента тега свойства работают вместе, чтобы отображать значения в списке и устанавливать соответствующие свойства при выборе элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="4007a-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="4007a-130">При первом отображении списка MAPI вызывает метод **опенпроперти** реализации **IMAPIProp** для получения таблицы, указанной в элементе **улпртабленаме** .</span><span class="sxs-lookup"><span data-stu-id="4007a-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="4007a-131">Количество столбцов в таблице зависит от значения элемента **улпрсетпроперти** .</span><span class="sxs-lookup"><span data-stu-id="4007a-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="4007a-132">Если для **улпрсетпроперти** задано значение **пр_нулл**, список является списком множественного выбора на основе объекта, содержащего получателей, например, контейнера адресной книги, таблицы получателей сообщения или таблицы содержимого списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="4007a-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="4007a-133">Таблица для списка множественного выбора должна содержать следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="4007a-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="4007a-134">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4007a-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="4007a-135">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4007a-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="4007a-136">**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4007a-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="4007a-137">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)), а также можно отобразить не более пяти других многозначных строковых свойств с тремя обязательными столбцами.</span><span class="sxs-lookup"><span data-stu-id="4007a-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="4007a-138">Если для члена **улпрсетпроперти** не задано значение **пр_нулл**, список является одним списком выбора.</span><span class="sxs-lookup"><span data-stu-id="4007a-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="4007a-139">Начальное значение **улпрсетпроперти** определяет первую выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4007a-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="4007a-140">Когда пользователь выбирает одну из строк, для элемента **улпрсетпроперти** задается выбранное значение, а это значение записывается обратно в реализацию интерфейса свойства с вызовом [IMAPIProp:: SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="4007a-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="4007a-141">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4007a-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4007a-142">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4007a-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4007a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="4007a-143">See also</span></span>



[<span data-ttu-id="4007a-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4007a-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="4007a-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4007a-145">MAPI Structures</span></span>](mapi-structures.md)

