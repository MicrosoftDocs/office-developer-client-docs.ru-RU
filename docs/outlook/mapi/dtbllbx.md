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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 04fbfb2e6938c1ae5971e90b30f5ef749e7963e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808358"
---
# <a name="dtbllbx"></a><span data-ttu-id="bc2eb-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="bc2eb-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="bc2eb-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc2eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc2eb-105">Описание списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc2eb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bc2eb-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc2eb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc2eb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="bc2eb-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="bc2eb-108">Members</span></span>

 <span data-ttu-id="bc2eb-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="bc2eb-109">**ulFlags**</span></span>
  
> <span data-ttu-id="bc2eb-110">Битовая маска флаги, используемые для устранения полосу прокрутки горизонтальный или вертикальный из списка.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="bc2eb-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="bc2eb-111">The following flags can be set:</span></span>
    
<span data-ttu-id="bc2eb-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="bc2eb-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="bc2eb-113">В списке должны быть отображены горизонтальной полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="bc2eb-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="bc2eb-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="bc2eb-115">Не вертикальная полоса прокрутки, отображаемые в списке.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="bc2eb-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="bc2eb-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="bc2eb-117">Свойство tag для свойства любого типа.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-117">Property tag for a property of any type.</span></span> <span data-ttu-id="bc2eb-118">Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableTable** .</span><span class="sxs-lookup"><span data-stu-id="bc2eb-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="bc2eb-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="bc2eb-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="bc2eb-120">Тег свойства для свойства в таблице типа PT_OBJECT, которая может быть открыта с помощью **OpenProperty** вызова.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="bc2eb-121">Число столбцов, которые должны иметь таблицы зависит от того, является ли список выделение одного или нескольких элементов списка.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="bc2eb-122">Если член **ulPRSetProperty** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), списке обеспечивает несколько фрагментов.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc2eb-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc2eb-123">Remarks</span></span>

<span data-ttu-id="bc2eb-124">Структура **DTBLLBX** описывает элемент управления, который используется для отображения нескольких элементов и позволяют пользователю выбрать одну или несколько элементов списка.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="bc2eb-125">**UlPRSetProperty** , а **ulPRTableName** работать вместе; При выборе одного значения из таблицы, он записывается обратно в **ulPRSetProperty** при диалоговое окно закрывается.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="bc2eb-126">Значение флагов указывает, следует ли отображать полосы прокрутки горизонтальный или вертикальный со списком.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="bc2eb-127">Значение по умолчанию — иметь типы прокрутки полосы отображаются, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="bc2eb-128">Поставщиков услуг можно задать MAPI_NO_HBAR для отмены вывода горизонтальной полосы прокрутки и MAPI_NO_VBAR для отмены вывода вертикальной полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="bc2eb-129">Элементы тега два свойства работают вместе для отображения значений в списке соответствующих свойств при выборе элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="bc2eb-130">Когда MAPI сначала отображается список, вызывает метод **OpenProperty** реализации **IMAPIProp** для получения таблицы, обнаруженных в элементе **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="bc2eb-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="bc2eb-131">Количество столбцов в таблице определяется значение элемента **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="bc2eb-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="bc2eb-132">Если **ulPRSetProperty** **PR_NULL**, список, несколько список выбора, основанный на объект, который содержит получателей, например контейнер адресной книги, таблице получателей сообщения или таблицу содержимого списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="bc2eb-133">Таблица для нескольких список выбора должен включать следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="bc2eb-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="bc2eb-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc2eb-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="bc2eb-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc2eb-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="bc2eb-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc2eb-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="bc2eb-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) и с тремя обязательные столбцы также может отображаться не более пяти другие свойства многозначных строковых.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="bc2eb-138">Если член **ulPRSetProperty** установлено значение **PR_NULL**, список, список выбора одного элемента.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="bc2eb-139">Начальное значение **ulPRSetProperty** определяет первой выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="bc2eb-140">При выборе одной из строк, — это набор элементов **ulPRSetProperty** на выбранное значение и это значение записывается обратно в реализации интерфейса свойства с помощью вызова [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="bc2eb-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="bc2eb-141">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bc2eb-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="bc2eb-142">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="bc2eb-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc2eb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="bc2eb-143">See also</span></span>



[<span data-ttu-id="bc2eb-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="bc2eb-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="bc2eb-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bc2eb-145">MAPI Structures</span></span>](mapi-structures.md)

