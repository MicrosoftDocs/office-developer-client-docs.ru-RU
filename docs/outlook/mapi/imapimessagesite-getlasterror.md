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
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420740"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="fb85b-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fb85b-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="fb85b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb85b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb85b-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объекте сайта сообщений.</span><span class="sxs-lookup"><span data-stu-id="fb85b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="fb85b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fb85b-106">Parameters</span></span>

 <span data-ttu-id="fb85b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="fb85b-107">_hResult_</span></span>
  
> <span data-ttu-id="fb85b-108">[in] HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="fb85b-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="fb85b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fb85b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fb85b-110">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="fb85b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="fb85b-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fb85b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fb85b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb85b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fb85b-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb85b-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="fb85b-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb85b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="fb85b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="fb85b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="fb85b-116">[вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb85b-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="fb85b-117">Этот параметр можно установить в NULL, если нет **структуры MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="fb85b-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb85b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb85b-118">Return value</span></span>

<span data-ttu-id="fb85b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb85b-119">S_OK</span></span>
  
> <span data-ttu-id="fb85b-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fb85b-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fb85b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fb85b-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="fb85b-122">Либо был MAPI_UNICODE флаг и **GetLastError** не поддерживает Unicode, либо MAPI_UNICODE не был установлен, **а GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="fb85b-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fb85b-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb85b-123">Remarks</span></span>

<span data-ttu-id="fb85b-124">Метод **IMAPIMessageSite::GetLastError** поставляет сведения о сбойного вызова предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="fb85b-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="fb85b-125">Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fb85b-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fb85b-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fb85b-126">Notes to callers</span></span>

<span data-ttu-id="fb85b-127">Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если MAPI поставляет один только в том случае, если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb85b-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="fb85b-128">Иногда MAPI не может определить, что была последняя ошибка, или не имеет ничего больше, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fb85b-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="fb85b-129">В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="fb85b-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="fb85b-130">Дополнительные сведения о **методе GetLastError** см. в рубрике [Использование расширенных ошибок.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="fb85b-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb85b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="fb85b-131">See also</span></span>



[<span data-ttu-id="fb85b-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fb85b-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fb85b-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb85b-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

