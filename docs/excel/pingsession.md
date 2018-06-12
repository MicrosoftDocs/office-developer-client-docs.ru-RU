---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807328"
---
# <a name="pingsession"></a><span data-ttu-id="8ab4b-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="8ab4b-103">PingSession</span></span>

<span data-ttu-id="8ab4b-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8ab4b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8ab4b-105">Проверяет, допустим ли сеанс.</span><span class="sxs-lookup"><span data-stu-id="8ab4b-105">Checks whether a session is valid.</span></span> <span data-ttu-id="8ab4b-106">Эта функция обычно вызывается, когда Excel необходимо определить, если ранее возвращенные сеанс остается активным и можно использовать.</span><span class="sxs-lookup"><span data-stu-id="8ab4b-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="8ab4b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ab4b-107">Parameters</span></span>

<span data-ttu-id="8ab4b-108">_Код сеанса_</span><span class="sxs-lookup"><span data-stu-id="8ab4b-108">_SessionID_</span></span>
  
> <span data-ttu-id="8ab4b-109">Идентификатор сеанса для проверки связи.</span><span class="sxs-lookup"><span data-stu-id="8ab4b-109">The ID of the session to ping.</span></span> <span data-ttu-id="8ab4b-110">Это значение должно соответствовать идентификатор, который возвращает предыдущего вызова [метод OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="8ab4b-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ab4b-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8ab4b-111">Return value</span></span>

<span data-ttu-id="8ab4b-112">**xlHpcRetSuccess** Если аргумент _SessionId_ является допустимым; в противном случае — **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="8ab4b-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ab4b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8ab4b-113">See also</span></span>

- [<span data-ttu-id="8ab4b-114">Метод OpenSession</span><span class="sxs-lookup"><span data-stu-id="8ab4b-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="8ab4b-115">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="8ab4b-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

