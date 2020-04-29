---
title: имаписессионжетластеррор
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
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435581"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="d1449-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d1449-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="d1449-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1449-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1449-105">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="d1449-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d1449-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1449-106">Parameters</span></span>

 <span data-ttu-id="d1449-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="d1449-107">_hResult_</span></span>
  
> <span data-ttu-id="d1449-108">возврата Дескриптор значения ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="d1449-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d1449-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1449-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d1449-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="d1449-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d1449-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d1449-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d1449-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1449-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d1449-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d1449-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d1449-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d1449-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d1449-115">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="d1449-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d1449-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="d1449-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d1449-117">Параметр _лппмапиеррор_ может иметь значение null, если MAPI не может предоставить соответствующую информацию для структуры **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="d1449-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d1449-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1449-118">Return value</span></span>

<span data-ttu-id="d1449-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1449-119">S_OK</span></span> 
  
> <span data-ttu-id="d1449-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d1449-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d1449-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d1449-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d1449-122">Установлен флаг MAPI_UNICODE, а сеанс не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="d1449-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1449-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1449-123">Remarks</span></span>

<span data-ttu-id="d1449-124">Метод **IMAPISession:: GetLastError** получает сведения о последней ошибке, возвращенной вызовом метода **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="d1449-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="d1449-125">Клиенты могут предоставить пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d1449-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1449-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d1449-126">Notes to callers</span></span>

<span data-ttu-id="d1449-127">Структуру **мапиеррор** можно использовать, если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="d1449-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d1449-128">Иногда MAPI не может определить, какая Последняя ошибка, или больше не содержит ничего больше об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d1449-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="d1449-129">В этом случае **GetLastError** возвращает указатель на значение NULL в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="d1449-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="d1449-130">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d1449-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1449-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d1449-131">See also</span></span>



[<span data-ttu-id="d1449-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d1449-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d1449-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d1449-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d1449-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1449-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d1449-135">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="d1449-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

