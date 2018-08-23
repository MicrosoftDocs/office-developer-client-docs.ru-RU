---
title: IMSProviderShutdown
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
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589093"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="eed73-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="eed73-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="eed73-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eed73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eed73-105">Закрывает поставщика хранилища сообщений определенным образом.</span><span class="sxs-lookup"><span data-stu-id="eed73-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eed73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eed73-106">Parameters</span></span>

 <span data-ttu-id="eed73-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="eed73-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="eed73-108">[in] Зарезервировано; должен быть указатель нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="eed73-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eed73-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="eed73-109">Return value</span></span>

<span data-ttu-id="eed73-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="eed73-110">S_OK</span></span> 
  
> <span data-ttu-id="eed73-111">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="eed73-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eed73-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="eed73-112">Remarks</span></span>

<span data-ttu-id="eed73-113">MAPI вызывает метод **IMSProvider::Shutdown** перед объект поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="eed73-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="eed73-114">MAPI освобождает все объекты входа в систему для поставщика, прежде чем вызывать **Завершение работы** для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="eed73-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eed73-115">См. также</span><span class="sxs-lookup"><span data-stu-id="eed73-115">See also</span></span>



[<span data-ttu-id="eed73-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eed73-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

