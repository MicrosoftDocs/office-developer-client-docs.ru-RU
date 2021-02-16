---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425205"
---
# <a name="validateparameters"></a><span data-ttu-id="57c03-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="57c03-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="57c03-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57c03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57c03-105">Вызывает внутреннюю функцию для проверки параметров, переданных клиентских приложений поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="57c03-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57c03-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="57c03-106">Header file:</span></span>  <br/> |<span data-ttu-id="57c03-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="57c03-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="57c03-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="57c03-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="57c03-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="57c03-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="57c03-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="57c03-110">Called by:</span></span>  <br/> |<span data-ttu-id="57c03-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="57c03-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="57c03-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="57c03-112">Parameters</span></span>

 <span data-ttu-id="57c03-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="57c03-113">_eMethod_</span></span>
  
> <span data-ttu-id="57c03-114">[in] Указывает метод для проверки с помощью enumeration.</span><span class="sxs-lookup"><span data-stu-id="57c03-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="57c03-115">_First_</span><span class="sxs-lookup"><span data-stu-id="57c03-115">_First_</span></span>
  
> <span data-ttu-id="57c03-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="57c03-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57c03-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57c03-117">Return value</span></span>

<span data-ttu-id="57c03-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="57c03-118">S_OK</span></span> 
  
> <span data-ttu-id="57c03-119">Допустимы все параметры.</span><span class="sxs-lookup"><span data-stu-id="57c03-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="57c03-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="57c03-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="57c03-121">Один или несколько параметров являются не допустимым.</span><span class="sxs-lookup"><span data-stu-id="57c03-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57c03-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="57c03-122">Remarks</span></span>

<span data-ttu-id="57c03-123">Макрос **ValidateParameters** был замелен макросом [ValidateParms.](validateparms.md)</span><span class="sxs-lookup"><span data-stu-id="57c03-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="57c03-124">**ValidateParameters** работает неправильно на платформах RISC и теперь не может на них компилироваться.</span><span class="sxs-lookup"><span data-stu-id="57c03-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="57c03-125">Он по-прежнему компилирует и корректно работает на платформах Intel, но **рекомендуется использовать ValidateParms** на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="57c03-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

