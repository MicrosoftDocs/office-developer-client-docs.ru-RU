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
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406033"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="5452a-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5452a-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="5452a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5452a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5452a-105">Управляет формой в представлении форм клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="5452a-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5452a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5452a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5452a-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="5452a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5452a-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="5452a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5452a-109">Просмотр объектов контекста</span><span class="sxs-lookup"><span data-stu-id="5452a-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="5452a-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5452a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5452a-111">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="5452a-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="5452a-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5452a-112">Called by:</span></span>  <br/> |<span data-ttu-id="5452a-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="5452a-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="5452a-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5452a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5452a-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="5452a-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="5452a-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5452a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5452a-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="5452a-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5452a-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="5452a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5452a-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5452a-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="5452a-120">Управляет регистрацией формы для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="5452a-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="5452a-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="5452a-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="5452a-122">Активирует следующее или предыдущее сообщение в представлении формы.</span><span class="sxs-lookup"><span data-stu-id="5452a-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="5452a-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="5452a-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="5452a-124">Извлекает текущие сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="5452a-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="5452a-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="5452a-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="5452a-126">Извлекает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="5452a-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="5452a-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="5452a-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="5452a-128">Извлекает текущее состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="5452a-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="5452a-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5452a-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="5452a-130">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте контекста представления.</span><span class="sxs-lookup"><span data-stu-id="5452a-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5452a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5452a-131">See also</span></span>



[<span data-ttu-id="5452a-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5452a-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

