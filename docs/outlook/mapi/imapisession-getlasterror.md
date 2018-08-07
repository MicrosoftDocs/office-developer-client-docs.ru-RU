---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809058"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="d8588-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d8588-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="d8588-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8588-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8588-105">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="d8588-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d8588-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8588-106">Parameters</span></span>

 <span data-ttu-id="d8588-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d8588-107">_hResult_</span></span>
  
> <span data-ttu-id="d8588-108">[in] Дескриптор значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="d8588-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d8588-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8588-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d8588-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="d8588-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d8588-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d8588-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d8588-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8588-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d8588-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d8588-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d8588-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d8588-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d8588-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d8588-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d8588-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8588-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d8588-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если MAPI не может предоставить соответствующие сведения для структуры **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="d8588-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8588-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d8588-118">Return value</span></span>

<span data-ttu-id="d8588-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d8588-119">S_OK</span></span> 
  
> <span data-ttu-id="d8588-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d8588-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d8588-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d8588-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d8588-122">Был установлен флажок MAPI_UNICODE и сеанса не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="d8588-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8588-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8588-123">Remarks</span></span>

<span data-ttu-id="d8588-124">Метод **IMAPISession::GetLastError** получает сведения о последней ошибки, возвращаемые для вызова метода **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="d8588-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="d8588-125">Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая эти сведения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d8588-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d8588-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d8588-126">Notes to callers</span></span>

<span data-ttu-id="d8588-127">Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="d8588-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d8588-128">В некоторых случаях MAPI не может определить последнюю ошибку был или он не более сообщить об ошибке содержит.</span><span class="sxs-lookup"><span data-stu-id="d8588-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="d8588-129">В этом случае **GetLastError** возвращает указатель на значение NULL в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="d8588-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="d8588-130">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d8588-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8588-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d8588-131">See also</span></span>



[<span data-ttu-id="d8588-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d8588-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d8588-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d8588-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d8588-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8588-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d8588-135">Расширенных ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="d8588-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

