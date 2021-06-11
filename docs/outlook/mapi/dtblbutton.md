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
# <a name="dtblbutton"></a><span data-ttu-id="8443d-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="8443d-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="8443d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8443d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8443d-105">Содержит сведения о том, как управлять кнопками для диалогового окна, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="8443d-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8443d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8443d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8443d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8443d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8443d-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="8443d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="8443d-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="8443d-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="8443d-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="8443d-110">Members</span></span>

 <span data-ttu-id="8443d-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="8443d-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="8443d-112">Положение в памяти строки символов, отображаемой на кнопке.</span><span class="sxs-lookup"><span data-stu-id="8443d-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="8443d-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8443d-113">**ulFlags**</span></span>
  
> <span data-ttu-id="8443d-114">Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="8443d-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="8443d-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8443d-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="8443d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8443d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8443d-117">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="8443d-117">The label is in Unicode format.</span></span> <span data-ttu-id="8443d-118">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="8443d-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="8443d-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="8443d-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="8443d-120">Тег свойства для свойства типа PT_OBJECT, реализуемого [интерфейсом IMAPIControl.](imapicontroliunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8443d-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="8443d-121">При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) таблицы отображения для получения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8443d-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8443d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="8443d-122">Remarks</span></span>

<span data-ttu-id="8443d-123">Структура **DTBLBUTTON** описывает кнопку управления, которая при нажатии позволяет пользователю приступить к операции.</span><span class="sxs-lookup"><span data-stu-id="8443d-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="8443d-124">Как правило, при нажатии кнопки отображается диалоговое окно modal или вызывается программатическая задача.</span><span class="sxs-lookup"><span data-stu-id="8443d-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="8443d-125">Поставщики услуг могут реализовать все, что угодно с помощью кнопки управления.</span><span class="sxs-lookup"><span data-stu-id="8443d-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="8443d-126">Если предполагается, что кнопка выполняет задачу на основе значений других элементов управления, эти элементы управления должны установить флаг DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="8443d-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="8443d-127">Член **ulbLpszLabel** — это положение в памяти строки символов, отображаемой на кнопке.</span><span class="sxs-lookup"><span data-stu-id="8443d-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="8443d-128">Поставщики услуг могут добавить символ ampersand () для обозначения Windows &amp; ускорителя на мете кнопки.</span><span class="sxs-lookup"><span data-stu-id="8443d-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="8443d-129">Нажатие клавиши акселератора имеет тот же эффект, что и нажатие кнопки.</span><span class="sxs-lookup"><span data-stu-id="8443d-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="8443d-130">Участник **ulPRControl** описывает свойство объекта, которое при открытом методе **IMAPIProp::OpenProperty** возвращает указатель на объект управления.</span><span class="sxs-lookup"><span data-stu-id="8443d-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="8443d-131">Реализация объекта управления, который поддерживает интерфейс **IMAPIControl,** позволяет расширить набор функций MAPI и определить операцию или задачу, которая возникает при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="8443d-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="8443d-132">**IMAPIControl** обеспечивает два метода управления кнопками: [GetState](imapicontrol-getstate.md) для отключения или включения кнопок и активации для обработки нажатий кнопки. [](imapicontrol-activate.md)</span><span class="sxs-lookup"><span data-stu-id="8443d-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="8443d-133">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="8443d-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="8443d-134">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="8443d-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8443d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="8443d-135">See also</span></span>



[<span data-ttu-id="8443d-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="8443d-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="8443d-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8443d-137">MAPI Structures</span></span>](mapi-structures.md)

