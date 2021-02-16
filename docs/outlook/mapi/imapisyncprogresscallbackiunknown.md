---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418339"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="002ff-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="002ff-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="002ff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="002ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="002ff-105">Передает поставщика магазина в качестве поля в структуре MAPISIB во время вызова [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="002ff-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="002ff-106">Поставщик магазина использует этот интерфейс для предоставления отзывов в Microsoft Outlook о состоянии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="002ff-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="002ff-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="002ff-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="002ff-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="002ff-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="002ff-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="002ff-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="002ff-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="002ff-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="002ff-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="002ff-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="002ff-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="002ff-112">Called by:</span></span>  <br/> |<span data-ttu-id="002ff-113">Поставщики магазина</span><span class="sxs-lookup"><span data-stu-id="002ff-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="002ff-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="002ff-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="002ff-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="002ff-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="002ff-116">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="002ff-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="002ff-117">Progress</span><span class="sxs-lookup"><span data-stu-id="002ff-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="002ff-118">Поставщик магазина периодически вызывает эту функцию для обновления состояния в диалоговом оке отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="002ff-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="002ff-119">Ошибка</span><span class="sxs-lookup"><span data-stu-id="002ff-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="002ff-120">Если во время синхронизации произошли ошибки, поставщик магазина вызывает эту функцию для предоставления сведений, отображаемой в диалоговом оке отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="002ff-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="002ff-121">Done</span><span class="sxs-lookup"><span data-stu-id="002ff-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="002ff-122">Поставщик магазина вызывает эту функцию, чтобы сообщить Outlook о том, что синхронизация завершена.</span><span class="sxs-lookup"><span data-stu-id="002ff-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="002ff-123">См. также</span><span class="sxs-lookup"><span data-stu-id="002ff-123">See also</span></span>



[<span data-ttu-id="002ff-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="002ff-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="002ff-125">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="002ff-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

