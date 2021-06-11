---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425878"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="ccabc-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ccabc-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="ccabc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccabc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccabc-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ccabc-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ccabc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ccabc-106">Parameters</span></span>

 <span data-ttu-id="ccabc-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ccabc-107">_hResult_</span></span>
  
> <span data-ttu-id="ccabc-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода для объекта хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ccabc-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="ccabc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccabc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ccabc-110">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="ccabc-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ccabc-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ccabc-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ccabc-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ccabc-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ccabc-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="ccabc-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ccabc-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ccabc-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ccabc-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ccabc-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ccabc-116">[вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="ccabc-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ccabc-117">Параметр _lppMAPIError может_ быть задан в NULL, если не будет **возвращен MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="ccabc-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ccabc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccabc-118">Return value</span></span>

<span data-ttu-id="ccabc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccabc-119">S_OK</span></span> 
  
> <span data-ttu-id="ccabc-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ccabc-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ccabc-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ccabc-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ccabc-122">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="ccabc-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccabc-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccabc-123">Remarks</span></span>

<span data-ttu-id="ccabc-124">Используйте **метод IMSLogon::GetLastError** для получения сведений, отображающихся в сообщении пользователю о последней ошибке, возвращаемой из вызова метода для объекта магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ccabc-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="ccabc-125">Чтобы освободить всю память, выделенную MAPI для возвращенной структуры **MAPIERROR,** клиентские приложения должны вызывать только функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ccabc-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="ccabc-126">Возвращаемая стоимость **getLastError** должна быть S_OK для приложения для использования **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="ccabc-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="ccabc-127">Даже если возвращаемая S_OK, **MAPIERROR** может не быть возвращена.</span><span class="sxs-lookup"><span data-stu-id="ccabc-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="ccabc-128">Если реализация не может определить последнюю ошибку или если **mapIERROR** недоступна для этой ошибки, **GetLastError** возвращает указатель nULL в  _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="ccabc-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccabc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ccabc-129">See also</span></span>



[<span data-ttu-id="ccabc-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ccabc-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ccabc-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ccabc-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ccabc-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccabc-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

