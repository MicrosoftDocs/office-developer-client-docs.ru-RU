---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584569"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="dcd37-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcd37-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="dcd37-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcd37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcd37-105">Управляет формы в форме просмотра клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="dcd37-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcd37-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dcd37-106">Header file:</span></span>  <br/> |<span data-ttu-id="dcd37-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="dcd37-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dcd37-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="dcd37-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dcd37-109">Просмотр объектов контекста</span><span class="sxs-lookup"><span data-stu-id="dcd37-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="dcd37-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dcd37-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dcd37-111">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="dcd37-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="dcd37-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dcd37-112">Called by:</span></span>  <br/> |<span data-ttu-id="dcd37-113">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="dcd37-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="dcd37-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="dcd37-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dcd37-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="dcd37-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="dcd37-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="dcd37-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dcd37-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="dcd37-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dcd37-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="dcd37-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dcd37-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dcd37-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="dcd37-120">Управляет формы регистрации для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="dcd37-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="dcd37-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="dcd37-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="dcd37-122">Активирует следующий или предыдущий сообщения в средстве просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="dcd37-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="dcd37-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="dcd37-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="dcd37-124">Извлекает сведения о текущем печати.</span><span class="sxs-lookup"><span data-stu-id="dcd37-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="dcd37-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="dcd37-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="dcd37-126">Получает поток, в который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcd37-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="dcd37-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="dcd37-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="dcd37-128">Извлекает текущее состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="dcd37-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="dcd37-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="dcd37-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="dcd37-130">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки, в объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="dcd37-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcd37-131">См. также</span><span class="sxs-lookup"><span data-stu-id="dcd37-131">See also</span></span>



[<span data-ttu-id="dcd37-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="dcd37-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

