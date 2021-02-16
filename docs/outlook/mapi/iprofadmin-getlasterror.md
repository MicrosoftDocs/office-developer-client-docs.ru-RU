---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430775"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="5cb9c-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5cb9c-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="5cb9c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cb9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cb9c-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="5cb9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cb9c-106">Parameters</span></span>

 <span data-ttu-id="5cb9c-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="5cb9c-107">_hResult_</span></span>
  
> <span data-ttu-id="5cb9c-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="5cb9c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5cb9c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5cb9c-110">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="5cb9c-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5cb9c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5cb9c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5cb9c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5cb9c-113">Строки в структуре [MAPIERROR,](mapierror.md) возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="5cb9c-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="5cb9c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5cb9c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5cb9c-116">[out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="5cb9c-117">Для _параметра lppMAPIError_ можно установить NULL, если не существует возвращаемой структуры **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="5cb9c-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5cb9c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cb9c-118">Return value</span></span>

<span data-ttu-id="5cb9c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5cb9c-119">S_OK</span></span> 
  
> <span data-ttu-id="5cb9c-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5cb9c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5cb9c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5cb9c-122">Либо флаг MAPI_UNICODE установлен и реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5cb9c-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="5cb9c-123">Remarks</span></span>

<span data-ttu-id="5cb9c-124">Метод **IProfAdmin::GetLastError** извлекает сведения о последней ошибке, возвращенной при вызове метода для объекта администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5cb9c-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5cb9c-125">Notes to callers</span></span>

<span data-ttu-id="5cb9c-126">Можно использовать структуру **MAPIERROR,** если MAPI передает ее, на нее указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="5cb9c-127">Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5cb9c-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="5cb9c-128">В этой ситуации указатель на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="5cb9c-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="5cb9c-129">Чтобы освободить всю память, выделенную MAPI для структуры **MAPIERROR,** вызовите функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="5cb9c-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="5cb9c-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных [сведениях об использовании расширенных ошибок.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="5cb9c-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5cb9c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5cb9c-131">See also</span></span>



[<span data-ttu-id="5cb9c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5cb9c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5cb9c-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5cb9c-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5cb9c-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5cb9c-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

