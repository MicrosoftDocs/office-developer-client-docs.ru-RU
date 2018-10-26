---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3426fd29090a6ab1bb0e66f9bb746e84abe3a25e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589450"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="08efd-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="08efd-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="08efd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08efd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08efd-105">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление сообщения объект сайта.</span><span class="sxs-lookup"><span data-stu-id="08efd-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="08efd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08efd-106">Parameters</span></span>

 <span data-ttu-id="08efd-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="08efd-107">_hResult_</span></span>
  
> <span data-ttu-id="08efd-108">[in] HRESULT, который содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="08efd-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="08efd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08efd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="08efd-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="08efd-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="08efd-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="08efd-111">The following flag can be set:</span></span>
    
<span data-ttu-id="08efd-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08efd-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="08efd-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="08efd-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="08efd-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="08efd-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="08efd-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="08efd-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="08efd-116">[out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="08efd-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="08efd-117">Этот параметр может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="08efd-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08efd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08efd-118">Return value</span></span>

<span data-ttu-id="08efd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="08efd-119">S_OK</span></span>
  
> <span data-ttu-id="08efd-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="08efd-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08efd-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="08efd-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="08efd-122">Либо был установлен флажок MAPI_UNICODE и **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="08efd-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08efd-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="08efd-123">Remarks</span></span>

<span data-ttu-id="08efd-124">Метод **IMAPIMessageSite::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="08efd-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="08efd-125">Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="08efd-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="08efd-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="08efd-126">Notes to callers</span></span>

<span data-ttu-id="08efd-127">Чтобы использовать **MAPIERROR** структуры, на который указывает с помощью параметра _lppMAPIError_ Если MAPI предоставляет только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="08efd-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="08efd-128">В некоторых случаях MAPI не может определить, что последней ошибкой был или не имеет никакого дополнительно, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="08efd-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="08efd-129">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="08efd-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="08efd-130">Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="08efd-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08efd-131">См. также</span><span class="sxs-lookup"><span data-stu-id="08efd-131">See also</span></span>



[<span data-ttu-id="08efd-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="08efd-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="08efd-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08efd-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

