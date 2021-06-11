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
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424429"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="6feaf-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6feaf-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="6feaf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6feaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6feaf-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="6feaf-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="6feaf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6feaf-106">Parameters</span></span>

 <span data-ttu-id="6feaf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="6feaf-107">_hResult_</span></span>
  
> <span data-ttu-id="6feaf-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="6feaf-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="6feaf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6feaf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6feaf-110">[in] Bitmask флагов, которые контролируют тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="6feaf-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="6feaf-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6feaf-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6feaf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6feaf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6feaf-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="6feaf-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="6feaf-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6feaf-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6feaf-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6feaf-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6feaf-116">[вышел] Указатель на указатель на возвращаемую структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="6feaf-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="6feaf-117">Этот параметр можно установить в NULL, если нет **структуры MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="6feaf-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6feaf-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6feaf-118">Return value</span></span>

<span data-ttu-id="6feaf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6feaf-119">S_OK</span></span> 
  
> <span data-ttu-id="6feaf-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6feaf-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6feaf-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6feaf-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6feaf-122">Либо был MAPI_UNICODE флаг, а **GetLastError** не поддерживает Unicode, либо MAPI_UNICODE не установлен, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="6feaf-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6feaf-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="6feaf-123">Remarks</span></span>

<span data-ttu-id="6feaf-124">Метод **IMAPIViewContext::GetLastError** поставляет сведения о сбойного вызова предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="6feaf-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="6feaf-125">Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6feaf-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6feaf-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6feaf-126">Notes to callers</span></span>

<span data-ttu-id="6feaf-127">Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если MAPI поставляет один только в том случае, если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="6feaf-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="6feaf-128">Иногда MAPI не может определить, какая последняя ошибка была или не имеет ничего больше, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6feaf-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="6feaf-129">В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="6feaf-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="6feaf-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="6feaf-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6feaf-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6feaf-131">See also</span></span>



[<span data-ttu-id="6feaf-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6feaf-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6feaf-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6feaf-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6feaf-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6feaf-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

