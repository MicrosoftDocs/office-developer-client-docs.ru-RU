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
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809195"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="6a844-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a844-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="6a844-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a844-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a844-105">Передает поставщика хранилища в качестве поля в структуре MAPISIB во время звонка на [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="6a844-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="6a844-106">Поставщик хранения использует этот интерфейс для Поделитесь своими впечатлениями о ходе выполнения синхронизации с Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="6a844-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a844-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6a844-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="6a844-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="6a844-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6a844-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="6a844-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="6a844-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="6a844-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a844-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="6a844-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="6a844-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="6a844-112">Called by:</span></span>  <br/> |<span data-ttu-id="6a844-113">Поставщики хранилища</span><span class="sxs-lookup"><span data-stu-id="6a844-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="6a844-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6a844-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a844-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="6a844-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6a844-116">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="6a844-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6a844-117">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="6a844-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="6a844-118">Поставщик хранения периодически вызывает эту функцию для обновления состояния в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="6a844-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="6a844-119">Error</span><span class="sxs-lookup"><span data-stu-id="6a844-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="6a844-120">Ошибки, возникающие во время синхронизации, поставщик хранения вызывает эту функцию для предоставления сведений, которые отображаются в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="6a844-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="6a844-121">Договорились</span><span class="sxs-lookup"><span data-stu-id="6a844-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="6a844-122">Поставщик хранения вызывает эту функцию для оповещения Outlook, синхронизация завершена.</span><span class="sxs-lookup"><span data-stu-id="6a844-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a844-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6a844-123">See also</span></span>



[<span data-ttu-id="6a844-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a844-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="6a844-125">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="6a844-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

