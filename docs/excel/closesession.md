---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807152"
---
# <a name="closesession"></a><span data-ttu-id="dd674-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="dd674-103">CloseSession</span></span>

<span data-ttu-id="dd674-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dd674-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dd674-105">Завершает сеанс в кластере.</span><span class="sxs-lookup"><span data-stu-id="dd674-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="dd674-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd674-106">Parameters</span></span>

<span data-ttu-id="dd674-107">_Код сеанса_</span><span class="sxs-lookup"><span data-stu-id="dd674-107">_SessionId_</span></span>
  
> <span data-ttu-id="dd674-108">Идентификатор сеанса, чтобы закрыть.</span><span class="sxs-lookup"><span data-stu-id="dd674-108">The ID of the session to close.</span></span> <span data-ttu-id="dd674-109">Это значение должно соответствовать значение, возвращенное [метод OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="dd674-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd674-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dd674-110">Return value</span></span>

<span data-ttu-id="dd674-111">**xlHpcRetSuccess** при закрытии сеанса; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на других ошибок.</span><span class="sxs-lookup"><span data-stu-id="dd674-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd674-112">См. также</span><span class="sxs-lookup"><span data-stu-id="dd674-112">See also</span></span>

- [<span data-ttu-id="dd674-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="dd674-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="dd674-114">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="dd674-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

