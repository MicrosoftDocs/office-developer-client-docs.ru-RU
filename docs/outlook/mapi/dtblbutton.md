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
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571068"
---
# <a name="dtblbutton"></a><span data-ttu-id="ebd9c-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="ebd9c-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="ebd9c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebd9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebd9c-105">Содержит сведения об элементе управления кнопки для диалогового окна, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebd9c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ebd9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebd9c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebd9c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ebd9c-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="ebd9c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ebd9c-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="ebd9c-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="ebd9c-110">Members</span><span class="sxs-lookup"><span data-stu-id="ebd9c-110">Members</span></span>

 <span data-ttu-id="ebd9c-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="ebd9c-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="ebd9c-112">Положение в памяти строки символ, отображаемый на кнопке.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="ebd9c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ebd9c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="ebd9c-114">Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="ebd9c-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="ebd9c-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ebd9c-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="ebd9c-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebd9c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ebd9c-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-117">The label is in Unicode format.</span></span> <span data-ttu-id="ebd9c-118">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="ebd9c-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="ebd9c-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="ebd9c-120">Свойство tag для свойства типа PT_OBJECT, который реализует интерфейс [IMAPIControl](imapicontroliunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd9c-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="ebd9c-121">При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) отображения таблицы для получения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebd9c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="ebd9c-122">Remarks</span></span>

<span data-ttu-id="ebd9c-123">Структура **DTBLBUTTON** описывает элемент управления кнопка, при нажатии этой кнопки, позволяющее начала операции.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="ebd9c-124">Как правило нажав кнопку вызывает модального диалогового окна для отображения или программные задачи для вызова.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="ebd9c-125">Поставщиков услуг можно реализовать все действия через элемент управления button.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="ebd9c-126">Если предполагается, что кнопки выполнения определенной задачи, на основе значений других элементов управления, эти элементы управления должны иметь флаг DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="ebd9c-127">Член **ulbLpszLabel** является позицию в памяти строки символ, отображаемый на кнопке.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="ebd9c-128">Поставщиков услуг можно добавить амперсанда (&amp;) для указания ускорителя Windows в метки кнопки.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="ebd9c-129">Нажав сочетание клавиш имеет тот же эффект, как нажатие кнопки.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="ebd9c-130">Член **ulPRControl** описывает свойства объекта, который, при открытии с помощью метода **IMAPIProp::OpenProperty** возвращает указатель на объект элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="ebd9c-131">Реализация объект элемента управления, который поддерживает интерфейс **IMAPIControl** — это способ расширить набор компонентов MAPI и определить операции или задачи, что происходит при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="ebd9c-132">**IMAPIControl** предоставляет два методы для работы с кнопками: [GetState](imapicontrol-getstate.md) , чтобы отключить или включить кнопки и [активировать](imapicontrol-activate.md) для обработки нажатий кнопок.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="ebd9c-133">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ebd9c-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ebd9c-134">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="ebd9c-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebd9c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ebd9c-135">See also</span></span>



[<span data-ttu-id="ebd9c-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ebd9c-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ebd9c-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd9c-137">MAPI Structures</span></span>](mapi-structures.md)

