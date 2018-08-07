---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808744"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="a4143-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="a4143-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="a4143-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4143-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4143-105">Отменяет подключение к активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4143-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a4143-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4143-106">Parameters</span></span>

 <span data-ttu-id="a4143-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4143-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a4143-108">[In] Зарезервировано; должен быть указатель нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a4143-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4143-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a4143-109">Return value</span></span>

<span data-ttu-id="a4143-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a4143-110">S_OK</span></span> 
  
> <span data-ttu-id="a4143-111">Подключение успешно отменено.</span><span class="sxs-lookup"><span data-stu-id="a4143-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a4143-112">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a4143-112">Notes to implementers</span></span>

<span data-ttu-id="a4143-113">В реализации метода **завершения работы** выполните любые задачи вам необходимо учитывать необходимые.</span><span class="sxs-lookup"><span data-stu-id="a4143-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="a4143-114">MAPI вызывает метод **Shutdown** только после выпустил всех объектов входа в систему.</span><span class="sxs-lookup"><span data-stu-id="a4143-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4143-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a4143-115">See also</span></span>



[<span data-ttu-id="a4143-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4143-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

