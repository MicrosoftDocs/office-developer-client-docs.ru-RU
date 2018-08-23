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
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578705"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="0e91e-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="0e91e-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="0e91e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e91e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e91e-105">Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг и MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e91e-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e91e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0e91e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e91e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0e91e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0e91e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0e91e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e91e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e91e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e91e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0e91e-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e91e-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0e91e-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="0e91e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e91e-112">Parameters</span></span>

 <span data-ttu-id="0e91e-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="0e91e-113">_eMethod_</span></span>
  
> <span data-ttu-id="0e91e-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="0e91e-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="0e91e-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="0e91e-115">_First_</span></span>
  
> <span data-ttu-id="0e91e-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="0e91e-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e91e-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0e91e-117">Return value</span></span>

<span data-ttu-id="0e91e-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0e91e-118">S_OK</span></span> 
  
> <span data-ttu-id="0e91e-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0e91e-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0e91e-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0e91e-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0e91e-121">Ошибка запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="0e91e-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e91e-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e91e-122">Remarks</span></span>

<span data-ttu-id="0e91e-123">Параметры, переданные между MAPI и службой поставщиков предполагается, что правильно и подвергаются только проверки отладка с помощью макроса [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="0e91e-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="0e91e-124">Поставщики должен проверить, все параметры, переданные в клиентских приложениях, но клиенты должны предполагается правильность параметров и MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e91e-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="0e91e-125">Использование макроса **HR_FAILED** для проверки возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0e91e-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="0e91e-126">Макрос **UlValidateParms** называется по-разному в зависимости от того, является ли вызывающий кода C или C++.</span><span class="sxs-lookup"><span data-stu-id="0e91e-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="0e91e-127">Этот макрос используется для проверки параметров несколько методы **IUnknown** и MAPI, которые возвращают ULONG вместо значения HRESULT; макрос [ValidateParms](validateparms.md) работает для всех других пользователей.</span><span class="sxs-lookup"><span data-stu-id="0e91e-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

