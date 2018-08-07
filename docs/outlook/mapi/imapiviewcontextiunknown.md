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
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809258"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="e3fd8-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3fd8-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="e3fd8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3fd8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3fd8-105">Управляет формы в форме просмотра клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3fd8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3fd8-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e3fd8-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e3fd8-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e3fd8-109">Просмотр объектов контекста</span><span class="sxs-lookup"><span data-stu-id="e3fd8-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="e3fd8-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3fd8-111">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="e3fd8-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e3fd8-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-112">Called by:</span></span>  <br/> |<span data-ttu-id="e3fd8-113">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="e3fd8-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="e3fd8-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e3fd8-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="e3fd8-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="e3fd8-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="e3fd8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e3fd8-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="e3fd8-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e3fd8-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="e3fd8-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e3fd8-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e3fd8-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="e3fd8-120">Управляет формы регистрации для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="e3fd8-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="e3fd8-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="e3fd8-122">Активирует следующий или предыдущий сообщения в средстве просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="e3fd8-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="e3fd8-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="e3fd8-124">Извлекает сведения о текущем печати.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="e3fd8-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="e3fd8-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="e3fd8-126">Получает поток, в который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="e3fd8-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="e3fd8-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="e3fd8-128">Извлекает текущее состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="e3fd8-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e3fd8-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="e3fd8-130">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки, в объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3fd8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e3fd8-131">See also</span></span>



[<span data-ttu-id="e3fd8-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="e3fd8-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

