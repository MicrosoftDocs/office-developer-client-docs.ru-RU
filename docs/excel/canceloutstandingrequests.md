---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414720"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="1f7b7-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="1f7b7-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="1f7b7-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f7b7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1f7b7-105">Информирует соединитель кластера о том, что вычисление Excel отменено, и, следовательно, все ожидающих вызовов функций в рамках этого сеанса также могут быть отменены (и Excel не ожидает перезвонков с их результатами).</span><span class="sxs-lookup"><span data-stu-id="1f7b7-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="1f7b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f7b7-106">Parameters</span></span>

<span data-ttu-id="1f7b7-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="1f7b7-107">_SessionID_</span></span>
  
> <span data-ttu-id="1f7b7-108">ИД сеанса, используемого отмененным вычислением.</span><span class="sxs-lookup"><span data-stu-id="1f7b7-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="1f7b7-109">Это значение соответствует значению, возвращаемом [OpenSession.](opensession.md)</span><span class="sxs-lookup"><span data-stu-id="1f7b7-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f7b7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f7b7-110">Return value</span></span>

<span data-ttu-id="1f7b7-111">**xlHpcRetSuccess,** если аргумент  _SessionId_ является допустимым; **xlHpcRetInvalidSessionId,** если аргумент  _SessionId_ является недопустимым; **xlHpcRetCallFailed при** других сбоях.</span><span class="sxs-lookup"><span data-stu-id="1f7b7-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f7b7-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f7b7-112">Remarks</span></span>

<span data-ttu-id="1f7b7-113">Для повышения производительности программа реализации должна остановить все процессы для сеанса, так как все результаты, полученные после этого вызова, будут отменены Excel.</span><span class="sxs-lookup"><span data-stu-id="1f7b7-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f7b7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1f7b7-114">See also</span></span>

- [<span data-ttu-id="1f7b7-115">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="1f7b7-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

