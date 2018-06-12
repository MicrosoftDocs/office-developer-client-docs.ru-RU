---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807142"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="0664f-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="0664f-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="0664f-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0664f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0664f-105">Информирует соединитель кластера, вычисления Excel отменена, и поэтому все ожидающие вызовы функций этого сеанса может быть отменен также (и, Excel не ожидается обратных вызовов с их результаты).</span><span class="sxs-lookup"><span data-stu-id="0664f-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="0664f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0664f-106">Parameters</span></span>

<span data-ttu-id="0664f-107">_Код сеанса_</span><span class="sxs-lookup"><span data-stu-id="0664f-107">_SessionID_</span></span>
  
> <span data-ttu-id="0664f-108">Идентификатор сеанса, используемые отмененные вычислений.</span><span class="sxs-lookup"><span data-stu-id="0664f-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="0664f-109">Это значение определяет соответствие значение, возвращенное [метод OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="0664f-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0664f-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0664f-110">Return value</span></span>

<span data-ttu-id="0664f-111">**xlHpcRetSuccess** Если аргумент _SessionId_ является допустимым; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на других ошибок.</span><span class="sxs-lookup"><span data-stu-id="0664f-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0664f-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="0664f-112">Remarks</span></span>

<span data-ttu-id="0664f-113">Специалистов по внедрению необходимо остановить все процессы для сеанса для повышения производительности, как никаких результатов, полученных после этот вызов не будет использоваться приложением Excel.</span><span class="sxs-lookup"><span data-stu-id="0664f-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0664f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0664f-114">See also</span></span>

- [<span data-ttu-id="0664f-115">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="0664f-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

