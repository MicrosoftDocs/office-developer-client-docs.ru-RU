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
description: 'Последнее изменение: 26 июня 2012 г.'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809196"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="fcea6-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="fcea6-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="fcea6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcea6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="fcea6-105">Запускает синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="fcea6-105">Initiates a synchronization.</span></span> <span data-ttu-id="fcea6-106">Этот метод вызывается с Microsoft Outlook 2010 и Microsoft Outlook 2013 и реализации поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="fcea6-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="fcea6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcea6-107">Parameters</span></span>

 <span data-ttu-id="fcea6-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="fcea6-108">_psibpb_</span></span>
  
> <span data-ttu-id="fcea6-109">О том, что будет синхронизирован с поставщиком и предоставляет доступ к интерфейсы, которые можно использовать во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fcea6-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="fcea6-110">Это структура [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="fcea6-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fcea6-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="fcea6-111">Return value</span></span>

<span data-ttu-id="fcea6-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="fcea6-112">S_OK</span></span> 
  
> <span data-ttu-id="fcea6-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fcea6-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcea6-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fcea6-114">See also</span></span>



[<span data-ttu-id="fcea6-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcea6-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="fcea6-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="fcea6-116">MAPISIB</span></span>](mapisib.md)

