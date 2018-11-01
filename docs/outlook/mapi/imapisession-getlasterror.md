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
ms.openlocfilehash: 34de52693d8484abb28d2ee2f7b86f15e8bd037b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574106"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="a52ff-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a52ff-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="a52ff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a52ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a52ff-105">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="a52ff-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a52ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a52ff-106">Parameters</span></span>

 <span data-ttu-id="a52ff-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a52ff-107">_hResult_</span></span>
  
> <span data-ttu-id="a52ff-108">[in] Дескриптор значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="a52ff-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="a52ff-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a52ff-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a52ff-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a52ff-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a52ff-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a52ff-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a52ff-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a52ff-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a52ff-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a52ff-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a52ff-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a52ff-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a52ff-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a52ff-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a52ff-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="a52ff-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="a52ff-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если MAPI не может предоставить соответствующие сведения для структуры **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="a52ff-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a52ff-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a52ff-118">Return value</span></span>

<span data-ttu-id="a52ff-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a52ff-119">S_OK</span></span> 
  
> <span data-ttu-id="a52ff-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a52ff-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a52ff-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a52ff-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a52ff-122">Был установлен флажок MAPI_UNICODE и сеанса не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="a52ff-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a52ff-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="a52ff-123">Remarks</span></span>

<span data-ttu-id="a52ff-124">Метод **IMAPISession::GetLastError** получает сведения о последней ошибки, возвращаемые для вызова метода **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="a52ff-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="a52ff-125">Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая эти сведения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a52ff-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a52ff-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a52ff-126">Notes to callers</span></span>

<span data-ttu-id="a52ff-127">Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="a52ff-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a52ff-128">В некоторых случаях MAPI не может определить последнюю ошибку был или он не более сообщить об ошибке содержит.</span><span class="sxs-lookup"><span data-stu-id="a52ff-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="a52ff-129">В этом случае **GetLastError** возвращает указатель на значение NULL в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="a52ff-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="a52ff-130">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="a52ff-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a52ff-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a52ff-131">See also</span></span>



[<span data-ttu-id="a52ff-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a52ff-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a52ff-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a52ff-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a52ff-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a52ff-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a52ff-135">Расширенных ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="a52ff-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

