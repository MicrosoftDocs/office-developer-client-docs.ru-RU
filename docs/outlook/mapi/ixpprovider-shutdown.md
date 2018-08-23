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
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592607"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="4e1bd-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="4e1bd-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="4e1bd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e1bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e1bd-105">Закрывает вниз поставщика транспорта определенным образом.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4e1bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e1bd-106">Parameters</span></span>

 <span data-ttu-id="4e1bd-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e1bd-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="4e1bd-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e1bd-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4e1bd-109">Return value</span></span>

<span data-ttu-id="4e1bd-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4e1bd-110">S_OK</span></span> 
  
> <span data-ttu-id="4e1bd-111">Вызов успешно завершает работу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e1bd-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e1bd-112">Remarks</span></span>

<span data-ttu-id="4e1bd-113">Диспетчер очереди MAPI вызывает метод **IXPProvider::Shutdown** перед освобождение объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="4e1bd-114">Прежде чем вызывать **Завершение работы**MAPI освобождает все объекты входа в систему для поставщика.</span><span class="sxs-lookup"><span data-stu-id="4e1bd-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e1bd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4e1bd-115">See also</span></span>



[<span data-ttu-id="4e1bd-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="4e1bd-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="4e1bd-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e1bd-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

