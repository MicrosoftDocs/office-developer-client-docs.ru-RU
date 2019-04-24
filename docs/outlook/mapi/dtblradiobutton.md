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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339419"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="4262d-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="4262d-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="4262d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4262d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4262d-105">Описывает один переключатель, который будет частью группы переключателей.</span><span class="sxs-lookup"><span data-stu-id="4262d-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="4262d-106">Группа переключателей будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="4262d-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4262d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4262d-107">Header file:</span></span>  <br/> |<span data-ttu-id="4262d-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4262d-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4262d-109">Members</span><span class="sxs-lookup"><span data-stu-id="4262d-109">Members</span></span>

 <span data-ttu-id="4262d-110">**Улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="4262d-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="4262d-111">Позиция в памяти метки строки символов для переключателя.</span><span class="sxs-lookup"><span data-stu-id="4262d-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="4262d-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4262d-112">**ulFlags**</span></span>
  
> <span data-ttu-id="4262d-113">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабел** .</span><span class="sxs-lookup"><span data-stu-id="4262d-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="4262d-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4262d-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="4262d-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4262d-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4262d-116">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="4262d-116">The label is in Unicode format.</span></span> <span data-ttu-id="4262d-117">Если флаг МАПИ_УНИКОДЕ не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="4262d-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="4262d-118">**Улкбуттонс**</span><span class="sxs-lookup"><span data-stu-id="4262d-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="4262d-119">Количество кнопок в группе переключателей.</span><span class="sxs-lookup"><span data-stu-id="4262d-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="4262d-120">Структуры **дтблрадиобуттон** для остальных кнопок в группе должны содержаться в последовательных строках таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="4262d-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="4262d-121">Каждая из этих строк должна содержать одно и то же значение для элемента **улкбуттонс** .</span><span class="sxs-lookup"><span data-stu-id="4262d-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="4262d-122">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="4262d-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="4262d-123">Тег свойства для свойства типа ПТ_ЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="4262d-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="4262d-124">Первоначальный выбор в группе переключателей основан на начальном значении этого свойства.</span><span class="sxs-lookup"><span data-stu-id="4262d-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="4262d-125">Каждой кнопке в группе необходимо присвоить значение **улпроптаг** , равное одному и тому же свойству.</span><span class="sxs-lookup"><span data-stu-id="4262d-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="4262d-126">**Лретурнвалуе**</span><span class="sxs-lookup"><span data-stu-id="4262d-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="4262d-127">Уникальный номер, идентифицирующий выбранную кнопку.</span><span class="sxs-lookup"><span data-stu-id="4262d-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4262d-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4262d-128">Remarks</span></span>

<span data-ttu-id="4262d-129">Структура **дтблрадиобуттон** описывает переключатель и элемент управления "Кнопка", связанный с группой кнопок.</span><span class="sxs-lookup"><span data-stu-id="4262d-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="4262d-130">Можно проверить только одну кнопку в группе; Установка одной кнопки приводит к тому, что остальные кнопки в группе будут сброшены.</span><span class="sxs-lookup"><span data-stu-id="4262d-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="4262d-131">Количество кнопок — это количество переключателей в группе.</span><span class="sxs-lookup"><span data-stu-id="4262d-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="4262d-132">Структуры для других переключателей в группе должны находиться в последующих строках таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="4262d-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="4262d-133">Каждая из этих структур должна иметь одно и то же значение для числа кнопок.</span><span class="sxs-lookup"><span data-stu-id="4262d-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="4262d-134">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4262d-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4262d-135">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4262d-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4262d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="4262d-136">See also</span></span>



[<span data-ttu-id="4262d-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="4262d-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="4262d-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4262d-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="4262d-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="4262d-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="4262d-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4262d-140">MAPI Structures</span></span>](mapi-structures.md)

