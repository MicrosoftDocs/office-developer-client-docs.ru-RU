---
title: Имапивиевконтекст IUnknown
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
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="eb946-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb946-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="eb946-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb946-105">Управляет формой в средстве просмотра форм клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="eb946-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb946-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="eb946-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb946-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="eb946-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="eb946-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="eb946-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="eb946-109">Просмотр объектов контекста</span><span class="sxs-lookup"><span data-stu-id="eb946-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="eb946-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="eb946-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb946-111">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="eb946-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="eb946-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="eb946-112">Called by:</span></span>  <br/> |<span data-ttu-id="eb946-113">Объекты форм</span><span class="sxs-lookup"><span data-stu-id="eb946-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="eb946-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="eb946-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eb946-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="eb946-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="eb946-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="eb946-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="eb946-117">лпмапивиевконтекст</span><span class="sxs-lookup"><span data-stu-id="eb946-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eb946-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="eb946-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eb946-119">сетадвисесинк</span><span class="sxs-lookup"><span data-stu-id="eb946-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="eb946-120">Управляет регистрацией формы для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="eb946-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="eb946-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="eb946-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="eb946-122">Активирует следующее или предыдущее сообщение в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="eb946-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="eb946-123">жетпринтсетуп</span><span class="sxs-lookup"><span data-stu-id="eb946-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="eb946-124">Получает текущие сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="eb946-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="eb946-125">жетсавестреам</span><span class="sxs-lookup"><span data-stu-id="eb946-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="eb946-126">Получает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb946-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="eb946-127">жетвиевстатус</span><span class="sxs-lookup"><span data-stu-id="eb946-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="eb946-128">Получает текущее состояние средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="eb946-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="eb946-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="eb946-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="eb946-130">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте контекста представления.</span><span class="sxs-lookup"><span data-stu-id="eb946-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb946-131">См. также</span><span class="sxs-lookup"><span data-stu-id="eb946-131">See also</span></span>



[<span data-ttu-id="eb946-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="eb946-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

