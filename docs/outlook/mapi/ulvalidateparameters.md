---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431276"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="acff6-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="acff6-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="acff6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acff6-105">Вызывает внутреннюю функцию для проверки параметров клиентские приложения, которые передаются поставщикам услуг и MAPI.</span><span class="sxs-lookup"><span data-stu-id="acff6-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acff6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="acff6-106">Header file:</span></span>  <br/> |<span data-ttu-id="acff6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="acff6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="acff6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="acff6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="acff6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="acff6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="acff6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="acff6-110">Called by:</span></span>  <br/> |<span data-ttu-id="acff6-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="acff6-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="acff6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="acff6-112">Parameters</span></span>

 <span data-ttu-id="acff6-113">_Емесод_</span><span class="sxs-lookup"><span data-stu-id="acff6-113">_eMethod_</span></span>
  
> <span data-ttu-id="acff6-114">возврата Определяет, по перечислению, метод, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="acff6-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="acff6-115">_First_</span><span class="sxs-lookup"><span data-stu-id="acff6-115">_First_</span></span>
  
> <span data-ttu-id="acff6-116">возврата Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="acff6-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="acff6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acff6-117">Return value</span></span>

<span data-ttu-id="acff6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="acff6-118">S_OK</span></span> 
  
> <span data-ttu-id="acff6-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="acff6-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="acff6-120">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="acff6-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="acff6-121">Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.</span><span class="sxs-lookup"><span data-stu-id="acff6-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="acff6-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="acff6-122">Remarks</span></span>

<span data-ttu-id="acff6-123">Макрос **улвалидатепараметерс** был заменен макросом [улвалидатепармс](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="acff6-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="acff6-124">**Улвалидатепараметерс** работает неправильно на платформах RISC и теперь не может компилироваться.</span><span class="sxs-lookup"><span data-stu-id="acff6-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="acff6-125">Он по-прежнему компилирует и работает правильно на платформах Intel, но **улвалидатепармс** рекомендуется на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="acff6-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

