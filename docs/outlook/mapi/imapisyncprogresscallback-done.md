---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573210"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="add01-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="add01-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="add01-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="add01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="add01-105">Информирует Microsoft Outlook, что синхронизация завершена.</span><span class="sxs-lookup"><span data-stu-id="add01-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="add01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="add01-106">Parameters</span></span>

 <span data-ttu-id="add01-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="add01-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="add01-108">Событие, которое передается обратно, чтобы разрешить Microsoft Outlook закрыть дескриптор.</span><span class="sxs-lookup"><span data-stu-id="add01-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="add01-109">Это может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="add01-109">It can be NULL.</span></span>
    
 <span data-ttu-id="add01-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="add01-110">**hResult**</span></span>
  
> <span data-ttu-id="add01-111">Значение HRESULT, указывающее, конечный статус хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="add01-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="add01-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="add01-112">Return value</span></span>

<span data-ttu-id="add01-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="add01-113">S_OK</span></span> 
  
> <span data-ttu-id="add01-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="add01-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="add01-115">См. также</span><span class="sxs-lookup"><span data-stu-id="add01-115">See also</span></span>



[<span data-ttu-id="add01-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="add01-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

