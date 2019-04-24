---
title: Имспровидершутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317264"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="587ed-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="587ed-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="587ed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="587ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="587ed-105">ЗаКрывает поставщик хранилища сообщений в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="587ed-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="587ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="587ed-106">Parameters</span></span>

 <span data-ttu-id="587ed-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="587ed-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="587ed-108">возврата Резервирования должен быть нулевым указателем.</span><span class="sxs-lookup"><span data-stu-id="587ed-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="587ed-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="587ed-109">Return value</span></span>

<span data-ttu-id="587ed-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="587ed-110">S_OK</span></span> 
  
> <span data-ttu-id="587ed-111">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="587ed-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="587ed-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="587ed-112">Remarks</span></span>

<span data-ttu-id="587ed-113">MAPI вызывает метод **функцииimsprovider:: Shutdown** непосредственно перед освобождением объекта поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="587ed-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="587ed-114">MAPI освобождает все объекты входа для поставщика до **завершения** вызова для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="587ed-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="587ed-115">См. также</span><span class="sxs-lookup"><span data-stu-id="587ed-115">See also</span></span>



[<span data-ttu-id="587ed-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="587ed-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

