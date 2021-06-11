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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434601"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="f9990-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f9990-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="f9990-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9990-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9990-105">Описывает одну кнопку радио, которая будет частью группы кнопок радио.</span><span class="sxs-lookup"><span data-stu-id="f9990-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="f9990-106">Группа кнопок радио будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="f9990-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9990-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f9990-107">Header file:</span></span>  <br/> |<span data-ttu-id="f9990-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9990-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f9990-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="f9990-109">Members</span></span>

 <span data-ttu-id="f9990-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="f9990-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="f9990-111">Положение в памяти метки строки символов для кнопки радио.</span><span class="sxs-lookup"><span data-stu-id="f9990-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="f9990-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f9990-112">**ulFlags**</span></span>
  
> <span data-ttu-id="f9990-113">Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="f9990-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="f9990-114">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f9990-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="f9990-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9990-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f9990-116">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9990-116">The label is in Unicode format.</span></span> <span data-ttu-id="f9990-117">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f9990-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="f9990-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="f9990-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="f9990-119">Количество кнопок в группе кнопки радио.</span><span class="sxs-lookup"><span data-stu-id="f9990-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="f9990-120">Структуры **DTBLRADIOBUTTON** для других кнопок в группе должны содержаться в последовательных строках таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="f9990-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="f9990-121">Каждая из этих строк должна содержать одинаковое значение для **члена ulcButtons.**</span><span class="sxs-lookup"><span data-stu-id="f9990-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="f9990-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="f9990-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="f9990-123">Тег свойства для свойства типа PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="f9990-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="f9990-124">Начальный выбор в группе кнопок радио основан на начальном значении этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f9990-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="f9990-125">Каждая кнопка в группе должна иметь **набор ulPropTag** к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="f9990-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="f9990-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="f9990-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="f9990-127">Уникальный номер, идентифицирует выбранную кнопку.</span><span class="sxs-lookup"><span data-stu-id="f9990-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9990-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9990-128">Remarks</span></span>

<span data-ttu-id="f9990-129">Структура **DTBLRADIOBUTTON** описывает кнопку радио кнопку управления кнопкой, которая связана с группой кнопок.</span><span class="sxs-lookup"><span data-stu-id="f9990-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="f9990-130">Проверить можно только одну кнопку в группе; установка одной кнопки приводит к отсечению других кнопок в группе.</span><span class="sxs-lookup"><span data-stu-id="f9990-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="f9990-131">Количество кнопок — это количество кнопок радио в группе.</span><span class="sxs-lookup"><span data-stu-id="f9990-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="f9990-132">Структуры для других кнопок радио в группе должны быть в последующих строках в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="f9990-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="f9990-133">Каждая из этих структур должна иметь одинаковое значение для подсчета кнопок.</span><span class="sxs-lookup"><span data-stu-id="f9990-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="f9990-134">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="f9990-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f9990-135">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="f9990-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9990-136">См. также</span><span class="sxs-lookup"><span data-stu-id="f9990-136">See also</span></span>



[<span data-ttu-id="f9990-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="f9990-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="f9990-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f9990-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="f9990-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="f9990-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="f9990-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f9990-140">MAPI Structures</span></span>](mapi-structures.md)

