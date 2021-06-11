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
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409785"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="b9251-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="b9251-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="b9251-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9251-105">Отмена подключения к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="b9251-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b9251-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9251-106">Parameters</span></span>

 <span data-ttu-id="b9251-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9251-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b9251-108">[In] Зарезервировано; должно быть указателем на ноль.</span><span class="sxs-lookup"><span data-stu-id="b9251-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9251-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9251-109">Return value</span></span>

<span data-ttu-id="b9251-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9251-110">S_OK</span></span> 
  
> <span data-ttu-id="b9251-111">Подключение было успешно отменено.</span><span class="sxs-lookup"><span data-stu-id="b9251-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b9251-112">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b9251-112">Notes to implementers</span></span>

<span data-ttu-id="b9251-113">В реализации метода **Shutdown** выполните все необходимые задачи.</span><span class="sxs-lookup"><span data-stu-id="b9251-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="b9251-114">MAPI вызывает метод **выключения** только после того, как вы выпустили все объекты с логотипом.</span><span class="sxs-lookup"><span data-stu-id="b9251-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9251-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b9251-115">See also</span></span>



[<span data-ttu-id="b9251-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9251-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

