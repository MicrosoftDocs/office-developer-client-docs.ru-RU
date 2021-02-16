---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439851"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="d84bb-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d84bb-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="d84bb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d84bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d84bb-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="d84bb-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d84bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d84bb-106">Parameters</span></span>

 <span data-ttu-id="d84bb-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d84bb-107">_hResult_</span></span>
  
> <span data-ttu-id="d84bb-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="d84bb-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d84bb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d84bb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d84bb-110">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="d84bb-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d84bb-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d84bb-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d84bb-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d84bb-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d84bb-113">Строки в **ПАРАМЕТРе MAPIERROR,** возвращенные в  _параметре lppMAPIError,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d84bb-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d84bb-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d84bb-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d84bb-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d84bb-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d84bb-116">[out] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="d84bb-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d84bb-117">Для  _параметра lppMAPIError_ можно установить NULL, если **MAPIERROR** не возвращается.</span><span class="sxs-lookup"><span data-stu-id="d84bb-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d84bb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d84bb-118">Return value</span></span>

<span data-ttu-id="d84bb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d84bb-119">S_OK</span></span> 
  
> <span data-ttu-id="d84bb-120">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="d84bb-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d84bb-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d84bb-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d84bb-122">Либо флаг MAPI_UNICODE установлен, а **GetLastError** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="d84bb-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d84bb-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="d84bb-123">Remarks</span></span>

<span data-ttu-id="d84bb-124">Метод **IProviderAdmin::GetLastError** обеспечивает сведения о вызове предыдущего метода, который не удалось вызвать.</span><span class="sxs-lookup"><span data-stu-id="d84bb-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="d84bb-125">Вызыватели могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d84bb-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d84bb-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d84bb-126">Notes to callers</span></span>

<span data-ttu-id="d84bb-127">Вы можете использовать структуру **MAPIERROR,** если MAPI передает ее, на которую указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="d84bb-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d84bb-128">Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d84bb-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="d84bb-129">В этой ситуации указатель на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="d84bb-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="d84bb-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных [сведениях об использовании расширенных ошибок.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="d84bb-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d84bb-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d84bb-131">See also</span></span>



[<span data-ttu-id="d84bb-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d84bb-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d84bb-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d84bb-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d84bb-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d84bb-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

