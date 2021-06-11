---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434251"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="00c7c-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="00c7c-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="00c7c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c7c-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="00c7c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="00c7c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="00c7c-106">Parameters</span></span>

 <span data-ttu-id="00c7c-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="00c7c-107">_hResult_</span></span>
  
> <span data-ttu-id="00c7c-108">[in] Ручка к значению ошибки, сгенерированная в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="00c7c-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="00c7c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00c7c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="00c7c-110">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="00c7c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="00c7c-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="00c7c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="00c7c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00c7c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="00c7c-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="00c7c-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="00c7c-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="00c7c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="00c7c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="00c7c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="00c7c-116">[вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="00c7c-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="00c7c-117">Параметр  _lppMAPIError можно_ установить в NULL, если поставщик не может предоставить структуре **MAPIERROR** соответствующую информацию.</span><span class="sxs-lookup"><span data-stu-id="00c7c-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00c7c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00c7c-118">Return value</span></span>

<span data-ttu-id="00c7c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="00c7c-119">S_OK</span></span> 
  
> <span data-ttu-id="00c7c-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="00c7c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="00c7c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="00c7c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="00c7c-122">Либо был MAPI_UNICODE флаг, а поставщик адресной книги не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а поставщик адресной книги поддерживает только Unicode.</span><span class="sxs-lookup"><span data-stu-id="00c7c-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00c7c-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="00c7c-123">Remarks</span></span>

<span data-ttu-id="00c7c-124">Поставщики адресных книг реализуют **метод GetLastError,** чтобы предоставить сведения о сбойных вызовах предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="00c7c-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="00c7c-125">Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="00c7c-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00c7c-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="00c7c-126">Notes to callers</span></span>

<span data-ttu-id="00c7c-127">Вы можете использовать структуру **MAPIERROR,** на которую указывает параметр  _lppMAPIError,_ если поставщик адресной книги поставляет эту структуру и только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="00c7c-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="00c7c-128">Иногда поставщик адресной книги не может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="00c7c-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="00c7c-129">В этой ситуации поставщик адресных книг возвращает указатель на NULL в _lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="00c7c-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="00c7c-130">Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="00c7c-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00c7c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="00c7c-131">See also</span></span>



[<span data-ttu-id="00c7c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="00c7c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="00c7c-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00c7c-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00c7c-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00c7c-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

