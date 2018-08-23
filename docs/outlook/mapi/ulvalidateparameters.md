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
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585243"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="c1ec5-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="c1ec5-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="c1ec5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1ec5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1ec5-105">Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг и MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1ec5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c1ec5-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1ec5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c1ec5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c1ec5-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c1ec5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1ec5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1ec5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1ec5-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c1ec5-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1ec5-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c1ec5-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="c1ec5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1ec5-112">Parameters</span></span>

 <span data-ttu-id="c1ec5-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="c1ec5-113">_eMethod_</span></span>
  
> <span data-ttu-id="c1ec5-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="c1ec5-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="c1ec5-115">_First_</span></span>
  
> <span data-ttu-id="c1ec5-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1ec5-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c1ec5-117">Return value</span></span>

<span data-ttu-id="c1ec5-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c1ec5-118">S_OK</span></span> 
  
> <span data-ttu-id="c1ec5-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c1ec5-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c1ec5-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c1ec5-121">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1ec5-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="c1ec5-122">Remarks</span></span>

<span data-ttu-id="c1ec5-123">Макрос **UlValidateParameters** был заменен макрос [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ec5-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="c1ec5-124">**UlValidateParameters** не работает на платформах RISC и теперь запрещено компиляцию на них.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="c1ec5-125">По-прежнему компилирует и работает правильно на платформах, но **UlValidateParms** рекомендуется для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="c1ec5-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

