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
# <a name="ulvalidateparms"></a><span data-ttu-id="2ff91-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="2ff91-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="2ff91-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff91-105">Вызывает внутреннюю функцию для проверки параметров клиентские приложения, которые передаются поставщикам услуг и MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ff91-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ff91-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2ff91-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ff91-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2ff91-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2ff91-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2ff91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ff91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ff91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ff91-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2ff91-110">Called by:</span></span>  <br/> |<span data-ttu-id="2ff91-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2ff91-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="2ff91-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff91-112">Parameters</span></span>

 <span data-ttu-id="2ff91-113">_Емесод_</span><span class="sxs-lookup"><span data-stu-id="2ff91-113">_eMethod_</span></span>
  
> <span data-ttu-id="2ff91-114">возврата Определяет, по перечислению, метод, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="2ff91-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="2ff91-115">_First_</span><span class="sxs-lookup"><span data-stu-id="2ff91-115">_First_</span></span>
  
> <span data-ttu-id="2ff91-116">возврата Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="2ff91-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ff91-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff91-117">Return value</span></span>

<span data-ttu-id="2ff91-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff91-118">S_OK</span></span> 
  
> <span data-ttu-id="2ff91-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2ff91-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="2ff91-120">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="2ff91-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="2ff91-121">Не удалось завершить операцию из — за ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2ff91-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ff91-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ff91-122">Remarks</span></span>

<span data-ttu-id="2ff91-123">Параметры, передаваемые между MAPI и поставщиками услуг, считаются верными и подвергнуты отладке только при проверке с помощью макроса [чеккпармс](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff91-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="2ff91-124">Поставщики должны проверить все параметры, переданные клиентскими приложениями, но клиенты должны предполагать, что параметры MAPI и provider указаны правильно.</span><span class="sxs-lookup"><span data-stu-id="2ff91-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="2ff91-125">Используйте макрос **хр_фаилед** для проверки возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="2ff91-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="2ff91-126">Макрос **улвалидатепармс** вызывается по-разному в зависимости от того, является ли вызывающий код C или C++.</span><span class="sxs-lookup"><span data-stu-id="2ff91-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="2ff91-127">Этот макрос используется для проверки параметров для нескольких методов **IUnknown** и MAPI, возвращающих ulong, а не значений HRESULT; макрос [валидатепармс](validateparms.md) работает для всех остальных.</span><span class="sxs-lookup"><span data-stu-id="2ff91-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

