---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419613"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="d39bd-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="d39bd-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="d39bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d39bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d39bd-105">Вызывает внутреннюю функцию для проверки параметров, переданных клиентские приложения поставщикам услуг и MAPI.</span><span class="sxs-lookup"><span data-stu-id="d39bd-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d39bd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d39bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="d39bd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d39bd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d39bd-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d39bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d39bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d39bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d39bd-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d39bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="d39bd-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d39bd-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="d39bd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d39bd-112">Parameters</span></span>

 <span data-ttu-id="d39bd-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="d39bd-113">_eMethod_</span></span>
  
> <span data-ttu-id="d39bd-114">[in] Указывает метод для проверки с помощью enumeration.</span><span class="sxs-lookup"><span data-stu-id="d39bd-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="d39bd-115">_First_</span><span class="sxs-lookup"><span data-stu-id="d39bd-115">_First_</span></span>
  
> <span data-ttu-id="d39bd-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="d39bd-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d39bd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d39bd-117">Return value</span></span>

<span data-ttu-id="d39bd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d39bd-118">S_OK</span></span> 
  
> <span data-ttu-id="d39bd-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d39bd-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d39bd-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d39bd-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="d39bd-121">Ошибка не позволяет завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="d39bd-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d39bd-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d39bd-122">Remarks</span></span>

<span data-ttu-id="d39bd-123">Параметры, переданные между MAPI и поставщиками услуг, считаются правильными и проходят только проверку отладки с помощью макроса [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="d39bd-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="d39bd-124">Поставщики должны проверять все параметры, переданные клиентских приложений, но клиенты должны предполагать, что MAPI и параметры поставщика являются правильными.</span><span class="sxs-lookup"><span data-stu-id="d39bd-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="d39bd-125">Используйте **макрос HR_FAILED** для проверки возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d39bd-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="d39bd-126">Макрос **UlValidateParms** вызывается по-разному в зависимости от того, является ли код вызова C или C++.</span><span class="sxs-lookup"><span data-stu-id="d39bd-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="d39bd-127">Этот макрос используется для проверки параметров для нескольких методов **IUnknown** и MAPI, которые возвращают ULONG вместо значений HRESULT; Макрос [ValidateParms](validateparms.md) работает для всех остальных.</span><span class="sxs-lookup"><span data-stu-id="d39bd-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

