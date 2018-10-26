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
ms.openlocfilehash: 63ddf6fd8f61834c7a7faa910f70bfd98715a703
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591326"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="f802b-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f802b-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="f802b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f802b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f802b-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="f802b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f802b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f802b-106">Parameters</span></span>

 <span data-ttu-id="f802b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f802b-107">_hResult_</span></span>
  
> <span data-ttu-id="f802b-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="f802b-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="f802b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f802b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f802b-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f802b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f802b-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f802b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f802b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f802b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f802b-113">Строки в **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f802b-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f802b-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f802b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f802b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f802b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f802b-116">[out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f802b-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f802b-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если нет **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="f802b-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f802b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f802b-118">Return value</span></span>

<span data-ttu-id="f802b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f802b-119">S_OK</span></span> 
  
> <span data-ttu-id="f802b-120">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="f802b-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="f802b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f802b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f802b-122">Либо был установлен флажок MAPI_UNICODE и **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f802b-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f802b-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="f802b-123">Remarks</span></span>

<span data-ttu-id="f802b-124">Метод **IProviderAdmin::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="f802b-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="f802b-125">Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f802b-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f802b-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f802b-126">Notes to callers</span></span>

<span data-ttu-id="f802b-127">Можно использовать структуры **MAPIERROR** , если MAPI предоставляет, что параметр _lppMAPIError_ указывает только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="f802b-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="f802b-128">В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="f802b-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="f802b-129">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="f802b-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="f802b-130">Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f802b-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f802b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f802b-131">See also</span></span>



[<span data-ttu-id="f802b-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f802b-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f802b-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f802b-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f802b-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f802b-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

