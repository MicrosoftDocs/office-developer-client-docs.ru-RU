---
title: Иперсистмессаже IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309606"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="a8917-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8917-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="a8917-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8917-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8917-105">Позволяет читателям форм обрабатывать хранение формы и переходить между различными состояниями.</span><span class="sxs-lookup"><span data-stu-id="a8917-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8917-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8917-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8917-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="a8917-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a8917-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="a8917-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a8917-109">Объекты хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="a8917-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="a8917-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a8917-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8917-111">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="a8917-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="a8917-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a8917-112">Called by:</span></span>  <br/> |<span data-ttu-id="a8917-113">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="a8917-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a8917-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a8917-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a8917-115">Иид_иперсистмессаже</span><span class="sxs-lookup"><span data-stu-id="a8917-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="a8917-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a8917-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a8917-117">ЛППЕРСИСТМЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="a8917-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a8917-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="a8917-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a8917-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a8917-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="a8917-120">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке в объекте Form.</span><span class="sxs-lookup"><span data-stu-id="a8917-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="a8917-121">Идентификатор ClassID</span><span class="sxs-lookup"><span data-stu-id="a8917-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="a8917-122">Возвращает идентификатор, представляющий сервер форм, который может управлять формой.</span><span class="sxs-lookup"><span data-stu-id="a8917-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="a8917-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="a8917-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="a8917-124">Проверяет форму на наличие изменений, выполненных с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="a8917-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="a8917-125">Инитнев</span><span class="sxs-lookup"><span data-stu-id="a8917-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="a8917-126">Инициализирует новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8917-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="a8917-127">Load</span><span class="sxs-lookup"><span data-stu-id="a8917-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="a8917-128">ЗаГружает форму для указанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8917-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="a8917-129">Save</span><span class="sxs-lookup"><span data-stu-id="a8917-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="a8917-130">Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.</span><span class="sxs-lookup"><span data-stu-id="a8917-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="a8917-131">Савекомплетед</span><span class="sxs-lookup"><span data-stu-id="a8917-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="a8917-132">Уведомляет форму о завершении операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="a8917-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="a8917-133">Хандсоффмессаже</span><span class="sxs-lookup"><span data-stu-id="a8917-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="a8917-134">Заставляет форму выпустить текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8917-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8917-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8917-135">Remarks</span></span>

<span data-ttu-id="a8917-136">Для реализации интерфейса **иперсистмессаже** необходимы все формы.</span><span class="sxs-lookup"><span data-stu-id="a8917-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="a8917-137">**Иперсистмессаже** работает аналогично интерфейсу OLE [иперсистстораже](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a8917-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="a8917-138">Дополнительные сведения см. в разделе методы **иперсистстораже** .</span><span class="sxs-lookup"><span data-stu-id="a8917-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8917-139">См. также</span><span class="sxs-lookup"><span data-stu-id="a8917-139">See also</span></span>



[<span data-ttu-id="a8917-140">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a8917-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

