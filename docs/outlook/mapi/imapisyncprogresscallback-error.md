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
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809180"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="6da6a-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="6da6a-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="6da6a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6da6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6da6a-105">Сведения, которые отображаются в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="6da6a-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="6da6a-106">Ошибки, возникающие во время синхронизации, поставщик хранения вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="6da6a-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="6da6a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6da6a-107">Parameters</span></span>

 <span data-ttu-id="6da6a-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="6da6a-108">**hResult**</span></span>
  
> <span data-ttu-id="6da6a-109">Значение HRESULT сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="6da6a-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="6da6a-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="6da6a-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="6da6a-111">Указатель на строку, связанную с ошибкой для отображения.</span><span class="sxs-lookup"><span data-stu-id="6da6a-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6da6a-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6da6a-112">Return value</span></span>

<span data-ttu-id="6da6a-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6da6a-113">S_OK</span></span> 
  
> <span data-ttu-id="6da6a-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6da6a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6da6a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6da6a-115">See also</span></span>



[<span data-ttu-id="6da6a-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6da6a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

