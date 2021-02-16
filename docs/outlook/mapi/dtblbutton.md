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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412788"
---
# <a name="dtblbutton"></a><span data-ttu-id="7dfc7-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="7dfc7-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="7dfc7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dfc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dfc7-105">Содержит сведения об кнопке для диалоговых окна, построенных из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7dfc7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7dfc7-106">Header file:</span></span>  <br/> |<span data-ttu-id="7dfc7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7dfc7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7dfc7-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="7dfc7-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7dfc7-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="7dfc7-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="7dfc7-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="7dfc7-110">Members</span></span>

 <span data-ttu-id="7dfc7-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="7dfc7-112">Положение в памяти строки символов, отображаемой на кнопке.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="7dfc7-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-113">**ulFlags**</span></span>
  
> <span data-ttu-id="7dfc7-114">Битовая метка флагов, используемая для обозначения формата метки, на который указывает элемент **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="7dfc7-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7dfc7-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="7dfc7-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7dfc7-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7dfc7-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-117">The label is in Unicode format.</span></span> <span data-ttu-id="7dfc7-118">Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="7dfc7-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="7dfc7-120">Тег свойства для свойства типа PT_OBJECT, который реализует [интерфейс IMAPIControl.](imapicontroliunknown.md)</span><span class="sxs-lookup"><span data-stu-id="7dfc7-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="7dfc7-121">При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) таблицы отображения, чтобы получить это свойство.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7dfc7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="7dfc7-122">Remarks</span></span>

<span data-ttu-id="7dfc7-123">Структура **DTBLBUTTON** описывает кнопку, которая позволяет пользователю при нажатии на нее начать операцию.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="7dfc7-124">Обычно при нажатии кнопки отображается модальные диалоговые окна или вызывается программная задача.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="7dfc7-125">Поставщики услуг могут реализовать что угодно с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="7dfc7-126">Если кнопка должна выполнять задачу на основе значений других элементов управления, эти элементы управления должны установить флаг DT_SET_IMMEDIATE элементов управления.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="7dfc7-127">Член **ulbLpszLabel** — это положение в памяти строки символов, отображаемой на кнопке.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="7dfc7-128">Поставщики услуг могут добавить символ амперанд ( ) для обозначения &amp; ускорителя Windows в метку кнопки.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="7dfc7-129">Нажатие клавиши ускорителя имеет тот же эффект, что и нажатие кнопки.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="7dfc7-130">Член **ulPRControl** описывает свойство объекта, которое при открытом методе **IMAPIProp::OpenProperty** возвращает указатель на объект управления.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="7dfc7-131">Реализация объекта управления, который поддерживает интерфейс **IMAPIControl,** позволяет расширить набор функций MAPI и определить операцию или задачу, которая выполняется при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="7dfc7-132">**IMAPIControl** обеспечивает два метода управления кнопками: [GetState](imapicontrol-getstate.md) для отключения или включения кнопок и активации для обработки нажатий кнопок. [](imapicontrol-activate.md)</span><span class="sxs-lookup"><span data-stu-id="7dfc7-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="7dfc7-133">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="7dfc7-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="7dfc7-134">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="7dfc7-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dfc7-135">См. также</span><span class="sxs-lookup"><span data-stu-id="7dfc7-135">See also</span></span>



[<span data-ttu-id="7dfc7-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="7dfc7-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="7dfc7-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7dfc7-137">MAPI Structures</span></span>](mapi-structures.md)

