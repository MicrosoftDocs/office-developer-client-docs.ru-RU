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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438626"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="7819e-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="7819e-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="7819e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7819e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7819e-105">ЗаКрывает поставщик хранилища сообщений в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="7819e-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7819e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7819e-106">Parameters</span></span>

 <span data-ttu-id="7819e-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="7819e-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7819e-108">возврата Резервирования должен быть нулевым указателем.</span><span class="sxs-lookup"><span data-stu-id="7819e-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7819e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7819e-109">Return value</span></span>

<span data-ttu-id="7819e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7819e-110">S_OK</span></span> 
  
> <span data-ttu-id="7819e-111">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="7819e-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7819e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7819e-112">Remarks</span></span>

<span data-ttu-id="7819e-113">MAPI вызывает метод **функцииimsprovider:: Shutdown** непосредственно перед освобождением объекта поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7819e-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="7819e-114">MAPI освобождает все объекты входа для поставщика до **завершения** вызова для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="7819e-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7819e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7819e-115">See also</span></span>



[<span data-ttu-id="7819e-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7819e-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

