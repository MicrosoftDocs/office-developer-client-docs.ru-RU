---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 65bf7debcae1367ccad9e109242fd4a72839a94e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584928"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="4b454-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4b454-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="4b454-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b454-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b454-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли в объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="4b454-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="4b454-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b454-106">Parameters</span></span>

 <span data-ttu-id="4b454-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="4b454-107">_hResult_</span></span>
  
> <span data-ttu-id="4b454-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="4b454-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="4b454-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b454-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4b454-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="4b454-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="4b454-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4b454-111">The following flag can be set:</span></span>
    
<span data-ttu-id="4b454-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b454-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4b454-113">Строки в структуре [MAPIERROR](mapierror.md) , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4b454-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="4b454-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4b454-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="4b454-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="4b454-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="4b454-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b454-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="4b454-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="4b454-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4b454-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b454-118">Return value</span></span>

<span data-ttu-id="4b454-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b454-119">S_OK</span></span> 
  
> <span data-ttu-id="4b454-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4b454-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4b454-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4b454-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4b454-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="4b454-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b454-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b454-123">Remarks</span></span>

<span data-ttu-id="4b454-124">Метод **IProfAdmin::GetLastError** получает сведения о последней ошибки, возвращаемые при вызове метода для объекта администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="4b454-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4b454-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4b454-125">Notes to callers</span></span>

<span data-ttu-id="4b454-126">Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="4b454-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="4b454-127">В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="4b454-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="4b454-128">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="4b454-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="4b454-129">Для освобождения всех памяти, выделенной для структуры **MAPIERROR** MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4b454-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="4b454-130">Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="4b454-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b454-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4b454-131">See also</span></span>



[<span data-ttu-id="4b454-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="4b454-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="4b454-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4b454-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4b454-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b454-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

