---
title: Имаписессионжетластеррор
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338684"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="cef98-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="cef98-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="cef98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cef98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cef98-105">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="cef98-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="cef98-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cef98-106">Parameters</span></span>

 <span data-ttu-id="cef98-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="cef98-107">_hResult_</span></span>
  
> <span data-ttu-id="cef98-108">возврата Дескриптор значения ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="cef98-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="cef98-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cef98-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cef98-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="cef98-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="cef98-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cef98-111">The following flag can be set:</span></span>
    
<span data-ttu-id="cef98-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cef98-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cef98-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="cef98-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="cef98-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="cef98-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="cef98-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="cef98-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="cef98-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="cef98-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="cef98-117">Параметр _лппмапиеррор_ может иметь значение null, если MAPI не может предоставить соответствующую информацию для структуры **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="cef98-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cef98-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cef98-118">Return value</span></span>

<span data-ttu-id="cef98-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cef98-119">S_OK</span></span> 
  
> <span data-ttu-id="cef98-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="cef98-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cef98-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="cef98-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="cef98-122">Установлен флаг МАПИ_УНИКОДЕ, а сеанс не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="cef98-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cef98-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cef98-123">Remarks</span></span>

<span data-ttu-id="cef98-124">Метод **IMAPISession:: GetLastError** получает сведения о последней ошибке, возвращенной вызовом метода **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="cef98-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="cef98-125">Клиенты могут предоставить пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cef98-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cef98-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cef98-126">Notes to callers</span></span>

<span data-ttu-id="cef98-127">Структуру **мапиеррор** можно использовать, если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="cef98-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="cef98-128">Иногда MAPI не может определить, какая Последняя ошибка, или больше не содержит ничего больше об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cef98-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="cef98-129">В этом случае **GetLastError** возвращает указатель на значение NULL в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="cef98-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="cef98-130">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="cef98-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cef98-131">См. также</span><span class="sxs-lookup"><span data-stu-id="cef98-131">See also</span></span>



[<span data-ttu-id="cef98-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="cef98-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="cef98-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cef98-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cef98-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cef98-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="cef98-135">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="cef98-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

