---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2a20f0f48eebe2194bc92afb98a620f9b39bb88d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809112"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="b55c5-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b55c5-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="b55c5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b55c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b55c5-105">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей объект поддержки.</span><span class="sxs-lookup"><span data-stu-id="b55c5-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b55c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b55c5-106">Parameters</span></span>

 <span data-ttu-id="b55c5-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b55c5-107">_hResult_</span></span>
  
> <span data-ttu-id="b55c5-108">[in] Дескриптор значение ошибки, созданный в предыдущем вызове метода для объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="b55c5-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="b55c5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b55c5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b55c5-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="b55c5-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b55c5-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b55c5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b55c5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b55c5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b55c5-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b55c5-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b55c5-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b55c5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b55c5-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b55c5-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b55c5-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="b55c5-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b55c5-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура **MAPIERROR** с сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b55c5-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b55c5-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b55c5-118">Return value</span></span>

<span data-ttu-id="b55c5-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b55c5-119">S_OK</span></span> 
  
> <span data-ttu-id="b55c5-120">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="b55c5-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="b55c5-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b55c5-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b55c5-122">Либо был установлен флажок MAPI_UNICODE и MAPI не поддерживает Юникод, или MAPI_UNICODE не было установлено и MAPI поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b55c5-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b55c5-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="b55c5-123">Remarks</span></span>

<span data-ttu-id="b55c5-124">Метод **IMAPISupport::GetLastError** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="b55c5-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="b55c5-125">Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b55c5-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b55c5-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b55c5-126">Notes to callers</span></span>

<span data-ttu-id="b55c5-127">Указатель на структуру **MAPIERROR** можно использовать, если MAPI предоставляет один с помощью параметра _lppMAPIError_ только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b55c5-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b55c5-128">В некоторых случаях MAPI не может определить последнюю ошибку был или он не более отчет об ошибке содержит.</span><span class="sxs-lookup"><span data-stu-id="b55c5-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="b55c5-129">В этом случае _lppMAPIError_ возвращает указатель на значение NULL вместо этого.</span><span class="sxs-lookup"><span data-stu-id="b55c5-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="b55c5-130">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b55c5-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="b55c5-131">Для освобождения всех памяти, выделенной MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) для возвращаемых структуры **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="b55c5-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b55c5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b55c5-132">See also</span></span>



[<span data-ttu-id="b55c5-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b55c5-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b55c5-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b55c5-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b55c5-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b55c5-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="b55c5-136">Расширенных ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="b55c5-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

