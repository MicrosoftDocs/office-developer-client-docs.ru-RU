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
# <a name="dtbllbx"></a><span data-ttu-id="c0c59-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="c0c59-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="c0c59-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0c59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0c59-105">Описывает список, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="c0c59-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c59-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c0c59-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0c59-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0c59-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="c0c59-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c0c59-108">Members</span></span>

 <span data-ttu-id="c0c59-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c0c59-109">**ulFlags**</span></span>
  
> <span data-ttu-id="c0c59-110">Bitmask флагов, используемых для устранения горизонтальной или вертикальной панели прокрутки из списка.</span><span class="sxs-lookup"><span data-stu-id="c0c59-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="c0c59-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c0c59-111">The following flags can be set:</span></span>
    
<span data-ttu-id="c0c59-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="c0c59-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="c0c59-113">В списке не следует показывать горизонтальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c0c59-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="c0c59-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="c0c59-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="c0c59-115">В списке не следует показывать вертикальную планку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c0c59-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="c0c59-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="c0c59-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="c0c59-117">Тег свойства для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="c0c59-117">Property tag for a property of any type.</span></span> <span data-ttu-id="c0c59-118">Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableTable.**</span><span class="sxs-lookup"><span data-stu-id="c0c59-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="c0c59-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="c0c59-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="c0c59-120">Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью **вызова OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="c0c59-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="c0c59-121">Количество столбцов, которые должны иметься в таблице, зависит от того, является ли список одним или нескольким списком выбора.</span><span class="sxs-lookup"><span data-stu-id="c0c59-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="c0c59-122">Если для **члена ulPRSetProperty** установлено PR_NULL [(PidTagNull),](pidtagnull-canonical-property.md)в списке допускается несколько вариантов выбора. </span><span class="sxs-lookup"><span data-stu-id="c0c59-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0c59-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0c59-123">Remarks</span></span>

<span data-ttu-id="c0c59-124">Структура **DTBLLBX** описывает список элементов управления, используемых для показа нескольких элементов, и позволит пользователю выбрать один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="c0c59-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="c0c59-125">Член **ulPRSetProperty** и **член ulPRTableName** работают вместе; Когда из таблицы выбирается одно значение, оно возвращается в **ulPRSetProperty** при отклонении диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c0c59-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="c0c59-126">Значение флагов указывает, следует ли отображать в списке горизонтальную или вертикальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c0c59-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="c0c59-127">По умолчанию должны отображаться типы слитков прокрутки, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="c0c59-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="c0c59-128">Поставщики услуг могут MAPI_NO_HBAR для подавления горизонтальной панели прокрутки и MAPI_NO_VBAR для подавления вертикальной панели прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c0c59-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="c0c59-129">Два элемента тега свойств работают вместе, чтобы отображать значения в списке и устанавливать соответствующие свойства при выборе элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="c0c59-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="c0c59-130">Когда MAPI впервые отображает список, он вызывает метод **реализации IMAPIProperty** для получения таблицы, определенной в члене **ulPRTableName.** </span><span class="sxs-lookup"><span data-stu-id="c0c59-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="c0c59-131">Количество столбцов в таблице зависит от значения участника **ulPRSetProperty.**</span><span class="sxs-lookup"><span data-stu-id="c0c59-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="c0c59-132">Если **для ulPRSetProperty** установлено **PR_NULL,** список — это несколько списков выбора, основанных на объекте, который содержит получателей, таких как контейнер адресной книги, таблица получателей для сообщения или таблица контента списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c0c59-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="c0c59-133">Таблица для нескольких списков выбора должна включать следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="c0c59-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="c0c59-134">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c0c59-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="c0c59-135">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c0c59-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="c0c59-136">**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c0c59-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="c0c59-137">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)и не более пяти других многоценных свойств строк можно также отображать с помощью трех необходимых столбцов.</span><span class="sxs-lookup"><span data-stu-id="c0c59-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="c0c59-138">Если у **члена ulPRSetProperty** не установлено **PR_NULL,** список является единым списком выбора.</span><span class="sxs-lookup"><span data-stu-id="c0c59-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="c0c59-139">Начальное значение **ulPRSetProperty** определяет первую выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c0c59-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="c0c59-140">Когда пользователь выбирает одну из строк, член **ulPRSetProperty** заданной для выбранного значения, и это значение возвращается в реализацию интерфейса свойств с вызовом [на IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="c0c59-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="c0c59-141">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="c0c59-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c0c59-142">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="c0c59-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0c59-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c0c59-143">See also</span></span>



[<span data-ttu-id="c0c59-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c0c59-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c0c59-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c59-145">MAPI Structures</span></span>](mapi-structures.md)

