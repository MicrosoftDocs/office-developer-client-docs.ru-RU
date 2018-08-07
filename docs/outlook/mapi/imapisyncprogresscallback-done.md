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
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809185"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="75190-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="75190-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="75190-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75190-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="75190-105">Информирует Microsoft Outlook, что синхронизация завершена.</span><span class="sxs-lookup"><span data-stu-id="75190-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="75190-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75190-106">Parameters</span></span>

 <span data-ttu-id="75190-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="75190-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="75190-108">Событие, которое передается обратно, чтобы разрешить Microsoft Outlook закрыть дескриптор.</span><span class="sxs-lookup"><span data-stu-id="75190-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="75190-109">Это может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="75190-109">It can be NULL.</span></span>
    
 <span data-ttu-id="75190-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="75190-110">**hResult**</span></span>
  
> <span data-ttu-id="75190-111">Значение HRESULT, указывающее, конечный статус хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="75190-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75190-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="75190-112">Return value</span></span>

<span data-ttu-id="75190-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="75190-113">S_OK</span></span> 
  
> <span data-ttu-id="75190-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="75190-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75190-115">См. также</span><span class="sxs-lookup"><span data-stu-id="75190-115">See also</span></span>



[<span data-ttu-id="75190-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75190-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

