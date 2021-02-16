---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Дата последнего изменения: 26 июня 2012 года'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426858"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="eb66d-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="eb66d-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="eb66d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb66d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="eb66d-105">Инициирует синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="eb66d-105">Initiates a synchronization.</span></span> <span data-ttu-id="eb66d-106">Этот метод вызван Microsoft Outlook 2010, русская версия Microsoft Outlook 2013 и реализован поставщиками store сообщений.</span><span class="sxs-lookup"><span data-stu-id="eb66d-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="eb66d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb66d-107">Parameters</span></span>

 <span data-ttu-id="eb66d-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="eb66d-108">_psibpb_</span></span>
  
> <span data-ttu-id="eb66d-109">Сообщает поставщику о том, что будет синхронизировано, и предоставляет доступ к интерфейсам, которые можно использовать во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eb66d-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="eb66d-110">Это структура [MAPISIB.](mapisib.md)</span><span class="sxs-lookup"><span data-stu-id="eb66d-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb66d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb66d-111">Return value</span></span>

<span data-ttu-id="eb66d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb66d-112">S_OK</span></span> 
  
> <span data-ttu-id="eb66d-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="eb66d-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb66d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="eb66d-114">See also</span></span>



[<span data-ttu-id="eb66d-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb66d-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="eb66d-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="eb66d-116">MAPISIB</span></span>](mapisib.md)

