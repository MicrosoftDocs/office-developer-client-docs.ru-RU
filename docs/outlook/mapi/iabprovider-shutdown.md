---
title: Иабпровидершутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348904"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="5a916-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="5a916-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="5a916-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a916-105">ОтМеняет подключение к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="5a916-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5a916-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a916-106">Parameters</span></span>

 <span data-ttu-id="5a916-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="5a916-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5a916-108">Возврата Резервирования должен быть нулевым указателем.</span><span class="sxs-lookup"><span data-stu-id="5a916-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a916-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a916-109">Return value</span></span>

<span data-ttu-id="5a916-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a916-110">S_OK</span></span> 
  
> <span data-ttu-id="5a916-111">Подключение было успешно отменено.</span><span class="sxs-lookup"><span data-stu-id="5a916-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="5a916-112">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5a916-112">Notes to implementers</span></span>

<span data-ttu-id="5a916-113">Выполните все необходимые задачи в реализации метода **завершения работы** .</span><span class="sxs-lookup"><span data-stu-id="5a916-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="5a916-114">MAPI вызывает метод **завершения работы** только после того, как вы выпускали все объекты входа.</span><span class="sxs-lookup"><span data-stu-id="5a916-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a916-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5a916-115">See also</span></span>



[<span data-ttu-id="5a916-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a916-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

