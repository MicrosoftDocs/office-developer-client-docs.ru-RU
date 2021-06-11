---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419004"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="a2500-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a2500-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="a2500-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2500-105">Возвращает [структуру MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке в таблице.</span><span class="sxs-lookup"><span data-stu-id="a2500-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a2500-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2500-106">Parameters</span></span>

 <span data-ttu-id="a2500-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a2500-107">_hResult_</span></span>
  
> <span data-ttu-id="a2500-108">[in] HRESULT, содержащая ошибку, созданную в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="a2500-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="a2500-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2500-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a2500-110">[in] Bitmask флагов, которые контролируют тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a2500-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="a2500-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a2500-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a2500-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2500-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a2500-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="a2500-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a2500-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a2500-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a2500-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a2500-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a2500-116">[вышел] Указатель на указатель на возвращаемую структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="a2500-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="a2500-117">Параметр  _lppMAPIError может_ быть задан в NULL, если структура **MAPIERROR** с соответствующей информацией не может быть предоставлена.</span><span class="sxs-lookup"><span data-stu-id="a2500-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2500-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2500-118">Return value</span></span>

<span data-ttu-id="a2500-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2500-119">S_OK</span></span> 
  
> <span data-ttu-id="a2500-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a2500-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a2500-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a2500-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a2500-122">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="a2500-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2500-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2500-123">Remarks</span></span>

<span data-ttu-id="a2500-124">Метод **IMAPITable::GetLastError** возвращает подробные сведения, если они доступны, о сбойного вызова предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="a2500-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="a2500-125">Эти сведения можно отображать в сообщении или диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a2500-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a2500-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a2500-126">Notes to callers</span></span>

<span data-ttu-id="a2500-127">**Вызывай GetLastError всякий** раз, когда необходимо отобразить сведения об ошибке пользователю.</span><span class="sxs-lookup"><span data-stu-id="a2500-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="a2500-128">Вы можете использовать структуру [MAPIERROR,](mapierror.md) на что указывает параметр  _lppMAPIError,_ если объект таблицы поставляет один только в том случае, если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="a2500-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a2500-129">Иногда реализация таблицы не может определить, какая была последняя ошибка, или больше не имеет ничего, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a2500-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a2500-130">В этой ситуации указатель  _на lppMAPIError_ заданной nULL.</span><span class="sxs-lookup"><span data-stu-id="a2500-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="a2500-131">Чтобы освободить всю память, выделенную для **структуры MAPIERROR,** позвоните [в функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a2500-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a2500-132">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="a2500-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2500-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a2500-133">See also</span></span>



[<span data-ttu-id="a2500-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a2500-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a2500-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a2500-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a2500-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2500-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

