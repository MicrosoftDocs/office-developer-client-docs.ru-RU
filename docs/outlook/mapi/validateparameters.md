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
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586069"
---
# <a name="validateparameters"></a><span data-ttu-id="d2f8a-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="d2f8a-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="d2f8a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2f8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2f8a-105">Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2f8a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d2f8a-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2f8a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d2f8a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d2f8a-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d2f8a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2f8a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2f8a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2f8a-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d2f8a-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2f8a-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d2f8a-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="d2f8a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2f8a-112">Parameters</span></span>

 <span data-ttu-id="d2f8a-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="d2f8a-113">_eMethod_</span></span>
  
> <span data-ttu-id="d2f8a-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="d2f8a-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="d2f8a-115">_First_</span></span>
  
> <span data-ttu-id="d2f8a-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2f8a-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d2f8a-117">Return value</span></span>

<span data-ttu-id="d2f8a-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d2f8a-118">S_OK</span></span> 
  
> <span data-ttu-id="d2f8a-119">Все параметры являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="d2f8a-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d2f8a-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="d2f8a-121">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2f8a-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2f8a-122">Remarks</span></span>

<span data-ttu-id="d2f8a-123">Макрос **ValidateParameters** был заменен макрос [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f8a-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="d2f8a-124">**ValidateParameters** не работает на платформах RISC и теперь запрещено компиляцию на них.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="d2f8a-125">По-прежнему компилирует и работает правильно на платформах, но **ValidateParms** рекомендуется для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="d2f8a-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

