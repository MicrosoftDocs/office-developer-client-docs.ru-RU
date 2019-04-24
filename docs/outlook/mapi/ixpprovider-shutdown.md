---
title: Иксппровидершутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357199"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="015a3-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="015a3-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="015a3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="015a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="015a3-105">ЗаКрывает поставщик транспорта в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="015a3-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="015a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="015a3-106">Parameters</span></span>

 <span data-ttu-id="015a3-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="015a3-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="015a3-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="015a3-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="015a3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="015a3-109">Return value</span></span>

<span data-ttu-id="015a3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="015a3-110">S_OK</span></span> 
  
> <span data-ttu-id="015a3-111">Вызов завершился успешно при завершении работы поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="015a3-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="015a3-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="015a3-112">Remarks</span></span>

<span data-ttu-id="015a3-113">Диспетчер очереди MAPI вызывает метод **иксппровидер:: Shutdown** непосредственно перед освобождением объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="015a3-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="015a3-114">Перед **завершением**вызовов Служба MAPI освобождает все объекты входа для поставщика.</span><span class="sxs-lookup"><span data-stu-id="015a3-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="015a3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="015a3-115">See also</span></span>



[<span data-ttu-id="015a3-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="015a3-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="015a3-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="015a3-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

