---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426711"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="82932-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="82932-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="82932-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82932-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82932-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="82932-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="82932-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="82932-106">Parameters</span></span>

 <span data-ttu-id="82932-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="82932-107">_hResult_</span></span>
  
> <span data-ttu-id="82932-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="82932-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="82932-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82932-109">_ulFlags_</span></span>
  
> <span data-ttu-id="82932-110">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="82932-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="82932-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="82932-111">The following flag can be set:</span></span>
    
<span data-ttu-id="82932-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82932-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="82932-113">Строки в структуре [MAPIERROR,](mapierror.md) возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="82932-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="82932-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="82932-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="82932-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="82932-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="82932-116">[вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="82932-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="82932-117">Параметр _lppMAPIError можно_ установить в NULL, если форма не может предоставить соответствующую информацию для **структуры MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="82932-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82932-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82932-118">Return value</span></span>

<span data-ttu-id="82932-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="82932-119">S_OK</span></span> 
  
> <span data-ttu-id="82932-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="82932-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="82932-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="82932-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="82932-122">Либо был MAPI_UNICODE флаг, а поставщик адресной книги не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а поставщик адресной книги поддерживает только Unicode.</span><span class="sxs-lookup"><span data-stu-id="82932-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82932-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="82932-123">Remarks</span></span>

<span data-ttu-id="82932-124">Объекты формы реализуют **метод IPersistMessage::GetLastError,** чтобы предоставить сведения о сбойном вызове предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="82932-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="82932-125">Зрители форм могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="82932-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="82932-126">Вызов **GetLastError** не влияет на состояние формы.</span><span class="sxs-lookup"><span data-stu-id="82932-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="82932-127">Когда **GetLastError** возвращается, форма остается в состоянии, в которое она была до вызова.</span><span class="sxs-lookup"><span data-stu-id="82932-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82932-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="82932-128">Notes to callers</span></span>

<span data-ttu-id="82932-129">Можно использовать структуру **MAPIERROR,** если форма поставляет ее, которая указывается параметром  _lppMAPIError_ только в том случае, если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="82932-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="82932-130">Иногда форма не может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="82932-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="82932-131">В этой ситуации форма возвращает указатель на NULL в  _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="82932-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="82932-132">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="82932-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82932-133">См. также</span><span class="sxs-lookup"><span data-stu-id="82932-133">See also</span></span>



[<span data-ttu-id="82932-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="82932-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="82932-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="82932-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="82932-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82932-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

