---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435581"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="b1f9a-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1f9a-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="b1f9a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1f9a-105">Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b1f9a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b1f9a-106">Parameters</span></span>

 <span data-ttu-id="b1f9a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b1f9a-107">_hResult_</span></span>
  
> <span data-ttu-id="b1f9a-108">[in] Ручка к значению ошибки, сгенерированная в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b1f9a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1f9a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b1f9a-110">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b1f9a-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b1f9a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b1f9a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1f9a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1f9a-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b1f9a-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b1f9a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b1f9a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b1f9a-116">[вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b1f9a-117">Параметр _lppMAPIError можно_ установить в NULL, если MAPI не может предоставить соответствующую информацию для **структуры MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="b1f9a-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b1f9a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1f9a-118">Return value</span></span>

<span data-ttu-id="b1f9a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1f9a-119">S_OK</span></span> 
  
> <span data-ttu-id="b1f9a-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b1f9a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b1f9a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b1f9a-122">Флаг MAPI_UNICODE и сеанс не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1f9a-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1f9a-123">Remarks</span></span>

<span data-ttu-id="b1f9a-124">Метод **IMAPISession::GetLastError** извлекает сведения о последней ошибке, которая была возвращена вызовом метода **IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="b1f9a-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="b1f9a-125">Клиенты могут предоставить своим пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1f9a-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b1f9a-126">Notes to callers</span></span>

<span data-ttu-id="b1f9a-127">Вы можете использовать структуру **MAPIERROR,** если MAPI поставляет один, на который указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b1f9a-128">Иногда MAPI не может определить, какая была последняя ошибка, или она не имеет ничего больше, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="b1f9a-129">В этой ситуации **GetLastError** возвращает указатель на NULL в _lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="b1f9a-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b1f9a-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="b1f9a-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1f9a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b1f9a-131">See also</span></span>



[<span data-ttu-id="b1f9a-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b1f9a-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b1f9a-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b1f9a-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b1f9a-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1f9a-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b1f9a-135">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="b1f9a-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

