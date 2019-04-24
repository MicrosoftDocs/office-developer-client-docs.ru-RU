---
title: Имаписинкпрогресскаллбаккеррор
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341337"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="de9ba-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="de9ba-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="de9ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de9ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de9ba-105">Предоставляет сведения, отображаемые в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="de9ba-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="de9ba-106">Если во время синхронизации возникли ошибки, поставщик услуг хранения вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="de9ba-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="de9ba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de9ba-107">Parameters</span></span>

 <span data-ttu-id="de9ba-108">**Состав**</span><span class="sxs-lookup"><span data-stu-id="de9ba-108">**hResult**</span></span>
  
> <span data-ttu-id="de9ba-109">ЗНАЧЕНИЕ HRESULT ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="de9ba-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="de9ba-110">**Пвксзеррорстр**</span><span class="sxs-lookup"><span data-stu-id="de9ba-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="de9ba-111">Указатель на строку, связанную с отображаемой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="de9ba-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de9ba-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de9ba-112">Return value</span></span>

<span data-ttu-id="de9ba-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="de9ba-113">S_OK</span></span> 
  
> <span data-ttu-id="de9ba-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="de9ba-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de9ba-115">См. также</span><span class="sxs-lookup"><span data-stu-id="de9ba-115">See also</span></span>



[<span data-ttu-id="de9ba-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de9ba-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

