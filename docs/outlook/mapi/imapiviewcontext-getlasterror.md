---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f7455e9013f3bd9460ae5f4d876c135594840b68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809247"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="5ca7a-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5ca7a-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="5ca7a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ca7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ca7a-105">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="5ca7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ca7a-106">Parameters</span></span>

 <span data-ttu-id="5ca7a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="5ca7a-107">_hResult_</span></span>
  
> <span data-ttu-id="5ca7a-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="5ca7a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ca7a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5ca7a-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="5ca7a-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5ca7a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5ca7a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5ca7a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5ca7a-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="5ca7a-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="5ca7a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5ca7a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5ca7a-116">[out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="5ca7a-117">Этот параметр может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ca7a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="5ca7a-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5ca7a-119">S_OK</span></span> 
  
> <span data-ttu-id="5ca7a-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5ca7a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5ca7a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5ca7a-122">Либо был установлен флажок MAPI_UNICODE и **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5ca7a-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ca7a-123">Remarks</span></span>

<span data-ttu-id="5ca7a-124">Метод **IMAPIViewContext::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="5ca7a-125">Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ca7a-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5ca7a-126">Notes to callers</span></span>

<span data-ttu-id="5ca7a-127">Чтобы использовать **MAPIERROR** структуры, на который указывает с помощью параметра _lppMAPIError_ Если MAPI предоставляет только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="5ca7a-128">В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="5ca7a-129">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="5ca7a-130">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5ca7a-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ca7a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5ca7a-131">See also</span></span>



[<span data-ttu-id="5ca7a-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5ca7a-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5ca7a-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5ca7a-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5ca7a-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ca7a-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

