---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424933"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="35ba5-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="35ba5-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="35ba5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35ba5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35ba5-105">Предоставляет сведения, которые отображаются в диалоговом оке отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="35ba5-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="35ba5-106">Если во время синхронизации произошли ошибки, поставщик магазина вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="35ba5-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="35ba5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35ba5-107">Parameters</span></span>

 <span data-ttu-id="35ba5-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="35ba5-108">**hResult**</span></span>
  
> <span data-ttu-id="35ba5-109">HRESULT ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="35ba5-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="35ba5-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="35ba5-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="35ba5-111">Указатель на строку, связанную с отображаемой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="35ba5-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35ba5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35ba5-112">Return value</span></span>

<span data-ttu-id="35ba5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="35ba5-113">S_OK</span></span> 
  
> <span data-ttu-id="35ba5-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="35ba5-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35ba5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="35ba5-115">See also</span></span>



[<span data-ttu-id="35ba5-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35ba5-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

