---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567890"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="e0266-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="e0266-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="e0266-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0266-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0266-105">Отменяет подключение к активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="e0266-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e0266-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0266-106">Parameters</span></span>

 <span data-ttu-id="e0266-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0266-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e0266-108">[In] Зарезервировано; должен быть указатель нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e0266-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0266-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0266-109">Return value</span></span>

<span data-ttu-id="e0266-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0266-110">S_OK</span></span> 
  
> <span data-ttu-id="e0266-111">Подключение успешно отменено.</span><span class="sxs-lookup"><span data-stu-id="e0266-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e0266-112">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="e0266-112">Notes to implementers</span></span>

<span data-ttu-id="e0266-113">В реализации метода **завершения работы** выполните любые задачи вам необходимо учитывать необходимые.</span><span class="sxs-lookup"><span data-stu-id="e0266-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="e0266-114">MAPI вызывает метод **Shutdown** только после выпустил всех объектов входа в систему.</span><span class="sxs-lookup"><span data-stu-id="e0266-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0266-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e0266-115">See also</span></span>



[<span data-ttu-id="e0266-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0266-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

