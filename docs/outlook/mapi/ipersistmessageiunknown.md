---
title: IPersistMessage IUnknown
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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809518"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="a8cf0-103">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8cf0-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="a8cf0-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8cf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8cf0-105">Включение средств просмотра формы для обработки хранилища формы и для перехода между состояниями различные.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8cf0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8cf0-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a8cf0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a8cf0-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a8cf0-109">Сохранение объектам сообщения</span><span class="sxs-lookup"><span data-stu-id="a8cf0-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="a8cf0-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8cf0-111">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="a8cf0-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="a8cf0-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-112">Called by:</span></span>  <br/> |<span data-ttu-id="a8cf0-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="a8cf0-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a8cf0-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a8cf0-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="a8cf0-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="a8cf0-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a8cf0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a8cf0-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a8cf0-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a8cf0-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="a8cf0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a8cf0-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a8cf0-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="a8cf0-120">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="a8cf0-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="a8cf0-122">Возвращает идентификатор, представляющий сервера форм для управления формы.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="a8cf0-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="a8cf0-124">Проверяет формы для изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="a8cf0-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="a8cf0-126">Инициализирует новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-127">Нагрузки</span><span class="sxs-lookup"><span data-stu-id="a8cf0-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="a8cf0-128">Загружает формы для указанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-129">Сохранение</span><span class="sxs-lookup"><span data-stu-id="a8cf0-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="a8cf0-130">Сохраняет измененную форму сообщение, из которого его загрузки или создан.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="a8cf0-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="a8cf0-132">Уведомляет формы, которая сохранения завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="a8cf0-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="a8cf0-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="a8cf0-134">Приводит к освобождение сообщения, его текущей формы.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8cf0-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8cf0-135">Remarks</span></span>

<span data-ttu-id="a8cf0-136">Все формы необходимы для реализации интерфейса **IPersistMessage** .</span><span class="sxs-lookup"><span data-stu-id="a8cf0-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="a8cf0-137">**IPersistMessage** работает так же интерфейс OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a8cf0-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="a8cf0-138">Для получения дополнительных сведений см **IPersistStorage** методы.</span><span class="sxs-lookup"><span data-stu-id="a8cf0-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8cf0-139">См. также</span><span class="sxs-lookup"><span data-stu-id="a8cf0-139">See also</span></span>



[<span data-ttu-id="a8cf0-140">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a8cf0-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

