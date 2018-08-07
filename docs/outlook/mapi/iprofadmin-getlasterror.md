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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 250074b28b98269df58fecfcb2d178f73e26c571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809503"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="7d424-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7d424-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="7d424-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d424-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d424-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли в объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="7d424-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="7d424-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d424-106">Parameters</span></span>

 <span data-ttu-id="7d424-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="7d424-107">_hResult_</span></span>
  
> <span data-ttu-id="7d424-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="7d424-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="7d424-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d424-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7d424-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="7d424-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="7d424-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7d424-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7d424-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d424-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7d424-113">Строки в структуре [MAPIERROR](mapierror.md) , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7d424-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="7d424-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7d424-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="7d424-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7d424-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="7d424-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="7d424-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="7d424-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="7d424-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7d424-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="7d424-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7d424-119">S_OK</span></span> 
  
> <span data-ttu-id="7d424-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7d424-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7d424-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7d424-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7d424-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="7d424-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d424-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="7d424-123">Remarks</span></span>

<span data-ttu-id="7d424-124">Метод **IProfAdmin::GetLastError** получает сведения о последней ошибки, возвращаемые при вызове метода для объекта администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="7d424-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d424-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7d424-125">Notes to callers</span></span>

<span data-ttu-id="7d424-126">Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="7d424-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="7d424-127">В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="7d424-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="7d424-128">В этом случае указатель на значение NULL, возвращается в _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="7d424-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="7d424-129">Для освобождения всех памяти, выделенной для структуры **MAPIERROR** MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7d424-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="7d424-130">Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7d424-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d424-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7d424-131">See also</span></span>



[<span data-ttu-id="7d424-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="7d424-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="7d424-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7d424-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7d424-134">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d424-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

