---
title: Имаписинкпрогресскаллбакк IUnknown
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
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="8c4ba-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c4ba-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="8c4ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c4ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c4ba-105">Передает поставщик магазина в виде поля в структуре МАПИСИБ во время вызова [имаписинк: синчронизеинбаккграунд](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="8c4ba-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="8c4ba-106">Поставщик магазина использует этот интерфейс для обратной связи с Microsoft Outlook о состоянии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c4ba-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c4ba-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8c4ba-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="8c4ba-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="8c4ba-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8c4ba-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="8c4ba-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="8c4ba-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8c4ba-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c4ba-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="8c4ba-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="8c4ba-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8c4ba-112">Called by:</span></span>  <br/> |<span data-ttu-id="8c4ba-113">Поставщики услуг хранения</span><span class="sxs-lookup"><span data-stu-id="8c4ba-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="8c4ba-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8c4ba-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8c4ba-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="8c4ba-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8c4ba-116">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="8c4ba-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8c4ba-117">Progress</span><span class="sxs-lookup"><span data-stu-id="8c4ba-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="8c4ba-118">Поставщик хранилища периодически вызывает эту функцию для обновления состояния в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="8c4ba-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8c4ba-119">Ошибка</span><span class="sxs-lookup"><span data-stu-id="8c4ba-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="8c4ba-120">Если во время синхронизации возникли ошибки, поставщик услуг хранения вызывает эту функцию для предоставления сведений, отображаемых в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="8c4ba-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8c4ba-121">Done</span><span class="sxs-lookup"><span data-stu-id="8c4ba-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="8c4ba-122">Поставщик услуг Store вызывает эту функцию, чтобы сообщить Outlook о завершении синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c4ba-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c4ba-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8c4ba-123">See also</span></span>



[<span data-ttu-id="8c4ba-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c4ba-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="8c4ba-125">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8c4ba-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

