---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569745"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="13d72-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="13d72-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="13d72-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13d72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13d72-105">Описание одного переключателя, который будет частью группы переключателей.</span><span class="sxs-lookup"><span data-stu-id="13d72-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="13d72-106">В диалоговом окне, построенного из таблицы отображения будет использоваться группы переключателей.</span><span class="sxs-lookup"><span data-stu-id="13d72-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13d72-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="13d72-107">Header file:</span></span>  <br/> |<span data-ttu-id="13d72-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13d72-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="13d72-109">Members</span><span class="sxs-lookup"><span data-stu-id="13d72-109">Members</span></span>

 <span data-ttu-id="13d72-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="13d72-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="13d72-111">Положение в памяти метки строка символов для переключателя.</span><span class="sxs-lookup"><span data-stu-id="13d72-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="13d72-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="13d72-112">**ulFlags**</span></span>
  
> <span data-ttu-id="13d72-113">Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="13d72-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="13d72-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="13d72-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="13d72-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13d72-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="13d72-116">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="13d72-116">The label is in Unicode format.</span></span> <span data-ttu-id="13d72-117">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="13d72-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="13d72-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="13d72-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="13d72-119">Число кнопок в группе.</span><span class="sxs-lookup"><span data-stu-id="13d72-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="13d72-120">**DTBLRADIOBUTTON** структуры для кнопки группы должны быть включены в последовательных строк в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="13d72-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="13d72-121">Каждый из этих строк должен содержать такое же значение для элемента **ulcButtons** .</span><span class="sxs-lookup"><span data-stu-id="13d72-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="13d72-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="13d72-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="13d72-123">Свойство tag для свойства типа PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="13d72-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="13d72-124">Начальный выбор в группе основано на начальное значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="13d72-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="13d72-125">Всех кнопок в группе должен иметь значение одного свойства **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="13d72-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="13d72-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="13d72-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="13d72-127">Уникальный номер, идентифицирующий выбранной кнопки.</span><span class="sxs-lookup"><span data-stu-id="13d72-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13d72-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="13d72-128">Remarks</span></span>

<span data-ttu-id="13d72-129">Структура **DTBLRADIOBUTTON** описывает переключатель элемента управления кнопка, связанный с группой кнопок.</span><span class="sxs-lookup"><span data-stu-id="13d72-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="13d72-130">Можно проверить только одну кнопку в группе; При указании одной кнопкой других кнопок в группе, чтобы были не заданы.</span><span class="sxs-lookup"><span data-stu-id="13d72-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="13d72-131">Кнопка счетчик — число кнопок-переключателей в группе.</span><span class="sxs-lookup"><span data-stu-id="13d72-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="13d72-132">В следующих строках таблицы отображения должен быть структуры для остальных переключателей в группе.</span><span class="sxs-lookup"><span data-stu-id="13d72-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="13d72-133">Каждый из этих структур должен иметь такое же значение для его счетчик кнопка.</span><span class="sxs-lookup"><span data-stu-id="13d72-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="13d72-134">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="13d72-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="13d72-135">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="13d72-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="13d72-136">См. также</span><span class="sxs-lookup"><span data-stu-id="13d72-136">See also</span></span>



[<span data-ttu-id="13d72-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="13d72-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="13d72-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="13d72-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="13d72-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="13d72-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="13d72-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="13d72-140">MAPI Structures</span></span>](mapi-structures.md)

