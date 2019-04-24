---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338313"
---
# <a name="dtblbutton"></a><span data-ttu-id="037f2-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="037f2-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="037f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="037f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="037f2-105">Содержит сведения о элементе управления "Кнопка" для диалогового окна, созданного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="037f2-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="037f2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="037f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="037f2-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="037f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="037f2-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="037f2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="037f2-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="037f2-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="037f2-110">Members</span><span class="sxs-lookup"><span data-stu-id="037f2-110">Members</span></span>

 <span data-ttu-id="037f2-111">**Улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="037f2-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="037f2-112">Позиция в памяти строки символов, отображаемой на кнопке.</span><span class="sxs-lookup"><span data-stu-id="037f2-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="037f2-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="037f2-113">**ulFlags**</span></span>
  
> <span data-ttu-id="037f2-114">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабел** .</span><span class="sxs-lookup"><span data-stu-id="037f2-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="037f2-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="037f2-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="037f2-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="037f2-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="037f2-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="037f2-117">The label is in Unicode format.</span></span> <span data-ttu-id="037f2-118">Если флаг МАПИ_УНИКОДЕ не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="037f2-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="037f2-119">**Улпрконтрол**</span><span class="sxs-lookup"><span data-stu-id="037f2-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="037f2-120">Тег свойства для свойства типа ПТ_ОБЖЕКТ, реализующего интерфейс [имапиконтрол](imapicontroliunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="037f2-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="037f2-121">При нажатии кнопки MAPI вызывает метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) таблицы отображения, чтобы получить это свойство.</span><span class="sxs-lookup"><span data-stu-id="037f2-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="037f2-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="037f2-122">Remarks</span></span>

<span data-ttu-id="037f2-123">Структура **дтблбуттон** описывает кнопку элемента управления, которая при нажатии позволяет пользователю начать операцию.</span><span class="sxs-lookup"><span data-stu-id="037f2-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="037f2-124">Как правило, нажатие кнопки приводит к отображению модального диалогового окна или программной задачи для вызова.</span><span class="sxs-lookup"><span data-stu-id="037f2-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="037f2-125">Поставщики услуг могут реализовать что-либо с помощью элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="037f2-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="037f2-126">Если кнопка должна выполнять задачу на основе значений других элементов управления, эти элементы управления должны иметь установленный флаг ДТ_СЕТ_ИММЕДИАТЕ.</span><span class="sxs-lookup"><span data-stu-id="037f2-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="037f2-127">Элемент **улблпсзлабел** — это позиция в памяти строки символов, которая отображается на кнопке.</span><span class="sxs-lookup"><span data-stu-id="037f2-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="037f2-128">Поставщики услуг могут добавить символ амперсанда (&amp;), чтобы обозначить ускоритель Windows в метке кнопки.</span><span class="sxs-lookup"><span data-stu-id="037f2-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="037f2-129">Нажатие клавиши вызова эквивалентно нажатию кнопки.</span><span class="sxs-lookup"><span data-stu-id="037f2-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="037f2-130">Элемент **улпрконтрол** описывает свойство Object, которое при открытии с помощью метода **IMAPIProp:: опенпроперти** возвращает указатель на объект элемента управления.</span><span class="sxs-lookup"><span data-stu-id="037f2-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="037f2-131">Реализация объекта элемента управления, поддерживающего интерфейс **имапиконтрол** , позволяет расширить набор функций MAPI и определить операцию или задачу, выполняемую при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="037f2-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="037f2-132">**Имапиконтрол** предоставляет два метода для управления кнопками: [](imapicontrol-getstate.md) "с выходом" и "включить кнопки" и " [активировать](imapicontrol-activate.md) для обработки нажатий кнопок".</span><span class="sxs-lookup"><span data-stu-id="037f2-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="037f2-133">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="037f2-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="037f2-134">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="037f2-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="037f2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="037f2-135">See also</span></span>



[<span data-ttu-id="037f2-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="037f2-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="037f2-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="037f2-137">MAPI Structures</span></span>](mapi-structures.md)

