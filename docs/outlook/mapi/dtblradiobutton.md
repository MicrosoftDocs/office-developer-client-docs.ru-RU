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
# <a name="dtblradiobutton"></a><span data-ttu-id="3f363-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="3f363-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="3f363-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f363-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f363-105">Описывает один переключатель, который будет частью группы переключателей.</span><span class="sxs-lookup"><span data-stu-id="3f363-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="3f363-106">Группа переключателей будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="3f363-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f363-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3f363-107">Header file:</span></span>  <br/> |<span data-ttu-id="3f363-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3f363-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3f363-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3f363-109">Members</span></span>

 <span data-ttu-id="3f363-110">**улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="3f363-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="3f363-111">Позиция в памяти метки строки символов для переключателя.</span><span class="sxs-lookup"><span data-stu-id="3f363-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="3f363-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3f363-112">**ulFlags**</span></span>
  
> <span data-ttu-id="3f363-113">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабел** .</span><span class="sxs-lookup"><span data-stu-id="3f363-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="3f363-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3f363-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="3f363-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f363-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3f363-116">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="3f363-116">The label is in Unicode format.</span></span> <span data-ttu-id="3f363-117">Если флаг MAPI_UNICODE не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="3f363-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="3f363-118">**улкбуттонс**</span><span class="sxs-lookup"><span data-stu-id="3f363-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="3f363-119">Количество кнопок в группе переключателей.</span><span class="sxs-lookup"><span data-stu-id="3f363-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="3f363-120">Структуры **дтблрадиобуттон** для остальных кнопок в группе должны содержаться в последовательных строках таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="3f363-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="3f363-121">Каждая из этих строк должна содержать одно и то же значение для элемента **улкбуттонс** .</span><span class="sxs-lookup"><span data-stu-id="3f363-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="3f363-122">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="3f363-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="3f363-123">Тег свойства для свойства типа PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="3f363-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="3f363-124">Первоначальный выбор в группе переключателей основан на начальном значении этого свойства.</span><span class="sxs-lookup"><span data-stu-id="3f363-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="3f363-125">Каждой кнопке в группе необходимо присвоить значение **улпроптаг** , равное одному и тому же свойству.</span><span class="sxs-lookup"><span data-stu-id="3f363-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="3f363-126">**лретурнвалуе**</span><span class="sxs-lookup"><span data-stu-id="3f363-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="3f363-127">Уникальный номер, идентифицирующий выбранную кнопку.</span><span class="sxs-lookup"><span data-stu-id="3f363-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f363-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f363-128">Remarks</span></span>

<span data-ttu-id="3f363-129">Структура **дтблрадиобуттон** описывает переключатель и элемент управления "Кнопка", связанный с группой кнопок.</span><span class="sxs-lookup"><span data-stu-id="3f363-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="3f363-130">Можно проверить только одну кнопку в группе; Установка одной кнопки приводит к тому, что остальные кнопки в группе будут сброшены.</span><span class="sxs-lookup"><span data-stu-id="3f363-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="3f363-131">Количество кнопок — это количество переключателей в группе.</span><span class="sxs-lookup"><span data-stu-id="3f363-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="3f363-132">Структуры для других переключателей в группе должны находиться в последующих строках таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="3f363-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="3f363-133">Каждая из этих структур должна иметь одно и то же значение для числа кнопок.</span><span class="sxs-lookup"><span data-stu-id="3f363-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="3f363-134">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3f363-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3f363-135">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="3f363-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f363-136">См. также</span><span class="sxs-lookup"><span data-stu-id="3f363-136">See also</span></span>



[<span data-ttu-id="3f363-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="3f363-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="3f363-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3f363-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="3f363-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="3f363-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="3f363-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3f363-140">MAPI Structures</span></span>](mapi-structures.md)

