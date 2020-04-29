---
title: имаписинкпрогресскаллбаккдоне
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
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422350"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="bbcc1-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="bbcc1-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="bbcc1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbcc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="bbcc1-105">Информирует Microsoft Outlook о завершении синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bbcc1-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="bbcc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbcc1-106">Parameters</span></span>

 <span data-ttu-id="bbcc1-107">**хсреаддонивент**</span><span class="sxs-lookup"><span data-stu-id="bbcc1-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="bbcc1-108">Событие, которое передается обратно, чтобы разрешить приложению Microsoft Outlook закрыть этот дескриптор.</span><span class="sxs-lookup"><span data-stu-id="bbcc1-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="bbcc1-109">Может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bbcc1-109">It can be NULL.</span></span>
    
 <span data-ttu-id="bbcc1-110">**Состав**</span><span class="sxs-lookup"><span data-stu-id="bbcc1-110">**hResult**</span></span>
  
> <span data-ttu-id="bbcc1-111">Значение HRESULT, указывающее конечный статус хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="bbcc1-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbcc1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbcc1-112">Return value</span></span>

<span data-ttu-id="bbcc1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbcc1-113">S_OK</span></span> 
  
> <span data-ttu-id="bbcc1-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bbcc1-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbcc1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bbcc1-115">See also</span></span>



[<span data-ttu-id="bbcc1-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbcc1-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

