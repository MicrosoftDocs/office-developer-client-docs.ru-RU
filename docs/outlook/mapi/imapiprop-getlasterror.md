---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435833"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="09f6a-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="09f6a-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="09f6a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09f6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09f6a-105">Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке.</span><span class="sxs-lookup"><span data-stu-id="09f6a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="09f6a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="09f6a-106">Parameters</span></span>

 <span data-ttu-id="09f6a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="09f6a-107">_hResult_</span></span>
  
> <span data-ttu-id="09f6a-108">[in] Ручка кода ошибки, сгенерированная в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="09f6a-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="09f6a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09f6a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="09f6a-110">[in] Битмашка флагов, которая указывает формат текста, возвращаемого в структуре **MAPIERROR,** указываемого _на lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="09f6a-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="09f6a-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="09f6a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="09f6a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09f6a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09f6a-113">Строки должны быть в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="09f6a-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="09f6a-114">Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="09f6a-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="09f6a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="09f6a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="09f6a-116">[вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="09f6a-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="09f6a-117">Параметр  _lppMAPIError можно_ установить в NULL, если не будет возвращена информация об ошибке.</span><span class="sxs-lookup"><span data-stu-id="09f6a-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09f6a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09f6a-118">Return value</span></span>

<span data-ttu-id="09f6a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="09f6a-119">S_OK</span></span> 
  
> <span data-ttu-id="09f6a-120">Информация об ошибке была возвращена.</span><span class="sxs-lookup"><span data-stu-id="09f6a-120">The error information was returned.</span></span>
    
<span data-ttu-id="09f6a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="09f6a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="09f6a-122">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="09f6a-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09f6a-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="09f6a-123">Remarks</span></span>

<span data-ttu-id="09f6a-124">Метод **IMAPIProp::GetLastError** поставляет сведения о предыдущем вызове метода, который не удалось.</span><span class="sxs-lookup"><span data-stu-id="09f6a-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="09f6a-125">Клиенты могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="09f6a-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="09f6a-126">Все реализации **GetLastError,** предоставляемые MAPI, являются реализацией ANSI, за исключением [реализации IAddrBook.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="09f6a-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="09f6a-127">Метод **GetLastError,** включенный в **IAddrBook,** поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="09f6a-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="09f6a-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="09f6a-128">Notes to implementers</span></span>

<span data-ttu-id="09f6a-129">Сведения о внедрении этого метода удаленным поставщиком транспорта и о том, какие сообщения возвращает этот метод поставщику транспорта, так как определенные условия ошибок, которые приводят к различным значениям HRESULT, будут разными для различных поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="09f6a-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="09f6a-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="09f6a-130">Notes to callers</span></span>

<span data-ttu-id="09f6a-131">Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если **GetLastError** поставляет один, только если значение возврата S_OK.</span><span class="sxs-lookup"><span data-stu-id="09f6a-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="09f6a-132">Иногда **GetLastError не** может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="09f6a-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="09f6a-133">В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="09f6a-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="09f6a-134">Чтобы освободить память для **структуры MAPIERROR,** позвоните в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="09f6a-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="09f6a-135">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="09f6a-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09f6a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="09f6a-136">See also</span></span>



[<span data-ttu-id="09f6a-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09f6a-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="09f6a-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="09f6a-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="09f6a-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="09f6a-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="09f6a-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09f6a-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="09f6a-141">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="09f6a-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

