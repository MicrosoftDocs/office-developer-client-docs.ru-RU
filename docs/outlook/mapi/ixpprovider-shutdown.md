---
title: IXPProviderShutdown
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
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809641"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="b4bd2-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="b4bd2-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="b4bd2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4bd2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4bd2-105">Закрывает вниз поставщика транспорта определенным образом.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b4bd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4bd2-106">Parameters</span></span>

 <span data-ttu-id="b4bd2-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4bd2-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b4bd2-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4bd2-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b4bd2-109">Return value</span></span>

<span data-ttu-id="b4bd2-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b4bd2-110">S_OK</span></span> 
  
> <span data-ttu-id="b4bd2-111">Вызов успешно завершает работу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4bd2-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4bd2-112">Remarks</span></span>

<span data-ttu-id="b4bd2-113">Диспетчер очереди MAPI вызывает метод **IXPProvider::Shutdown** перед освобождение объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="b4bd2-114">Прежде чем вызывать **Завершение работы**MAPI освобождает все объекты входа в систему для поставщика.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4bd2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b4bd2-115">See also</span></span>



[<span data-ttu-id="b4bd2-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="b4bd2-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="b4bd2-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4bd2-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

