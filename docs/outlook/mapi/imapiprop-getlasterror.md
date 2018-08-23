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
ms.openlocfilehash: f67dbb4d883f2f66099f2e2b9bc06b6c35b98236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575835"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="eaa8f-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="eaa8f-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="eaa8f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaa8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaa8f-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="eaa8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaa8f-106">Parameters</span></span>

 <span data-ttu-id="eaa8f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="eaa8f-107">_hResult_</span></span>
  
> <span data-ttu-id="eaa8f-108">[in] Дескриптор код ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="eaa8f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eaa8f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="eaa8f-110">[in] Битовая маска флаги, которое указывает формат для текста, возвращаемых в структуре **MAPIERROR** , на который указывает _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="eaa8f-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="eaa8f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="eaa8f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eaa8f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eaa8f-113">Строки должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="eaa8f-114">Если флаг MAPI_UNICODE не установлен, строки должен быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="eaa8f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="eaa8f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="eaa8f-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="eaa8f-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если нет данных об ошибках для возврата.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eaa8f-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="eaa8f-118">Return value</span></span>

<span data-ttu-id="eaa8f-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="eaa8f-119">S_OK</span></span> 
  
> <span data-ttu-id="eaa8f-120">Возвращает сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-120">The error information was returned.</span></span>
    
<span data-ttu-id="eaa8f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="eaa8f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="eaa8f-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaa8f-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="eaa8f-123">Remarks</span></span>

<span data-ttu-id="eaa8f-124">Метод **IMAPIProp::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="eaa8f-125">Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="eaa8f-126">Все реализации **GetLastError** предоставлено MAPI, реализации ANSI, за исключением реализации [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="eaa8f-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="eaa8f-127">Метод **GetLastError** , включенные в состав **IAddrBook** поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eaa8f-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="eaa8f-128">Notes to implementers</span></span>

<span data-ttu-id="eaa8f-129">Сведения о удаленной транспорта поставщика реализация этого метода и какие сообщения, этот метод возвращает все периоды до поставщика транспорта, так как условия ошибки, которые привести к различные значения HRESULT будет отличаться для разных транспорта Поставщики.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="eaa8f-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="eaa8f-130">Notes to callers</span></span>

<span data-ttu-id="eaa8f-131">Можно использовать структуры **MAPIERROR** , указывает _lppMAPIError_ параметр, если **GetLastError** предоставляет, только в том случае, если возвращаемым значением является значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="eaa8f-132">В некоторых случаях **GetLastError** не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="eaa8f-133">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="eaa8f-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="eaa8f-134">Чтобы освободить память для структуры **MAPIERROR** , вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="eaa8f-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="eaa8f-135">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="eaa8f-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eaa8f-136">См. также</span><span class="sxs-lookup"><span data-stu-id="eaa8f-136">See also</span></span>



[<span data-ttu-id="eaa8f-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eaa8f-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="eaa8f-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="eaa8f-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="eaa8f-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eaa8f-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eaa8f-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eaa8f-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="eaa8f-141">Расширенных ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="eaa8f-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

