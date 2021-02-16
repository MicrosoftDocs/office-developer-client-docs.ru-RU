---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417010"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="c938d-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c938d-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="c938d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c938d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c938d-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке объекта фабрики форм.</span><span class="sxs-lookup"><span data-stu-id="c938d-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c938d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c938d-106">Parameters</span></span>

 <span data-ttu-id="c938d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c938d-107">_hResult_</span></span>
  
> <span data-ttu-id="c938d-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="c938d-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="c938d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c938d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c938d-110">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="c938d-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c938d-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c938d-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="c938d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c938d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c938d-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="c938d-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c938d-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c938d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c938d-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c938d-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c938d-116">[out] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="c938d-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c938d-117">Этот параметр может иметь NULL, если не существует возвращаемой структуры **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="c938d-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c938d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c938d-118">Return value</span></span>

<span data-ttu-id="c938d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c938d-119">S_OK</span></span> 
  
> <span data-ttu-id="c938d-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c938d-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c938d-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c938d-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c938d-122">Либо флаг MAPI_UNICODE установлен, а **GetLastError** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="c938d-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c938d-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c938d-123">Remarks</span></span>

<span data-ttu-id="c938d-124">Метод **IMAPIFormFactory::GetLastError** передает сведения о вызове предыдущего метода, который не удалось вызвать.</span><span class="sxs-lookup"><span data-stu-id="c938d-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="c938d-125">Вызыватели могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c938d-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c938d-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c938d-126">Notes to callers</span></span>

<span data-ttu-id="c938d-127">Вы можете использовать структуру **MAPIERROR,** на которая указывает параметр  _lppMAPIError,_ если MAPI указывает ее только в том случае, если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="c938d-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c938d-128">Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c938d-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="c938d-129">В этой ситуации указатель на NULL возвращается _в lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="c938d-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="c938d-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных [сведениях об использовании расширенных ошибок.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="c938d-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c938d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c938d-131">See also</span></span>



[<span data-ttu-id="c938d-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c938d-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c938d-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c938d-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c938d-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c938d-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

