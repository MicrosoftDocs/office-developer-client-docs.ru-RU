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
# <a name="iablogongetlasterror"></a><span data-ttu-id="f9996-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f9996-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="f9996-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9996-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f9996-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f9996-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9996-106">Parameters</span></span>

 <span data-ttu-id="f9996-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f9996-107">_hResult_</span></span>
  
> <span data-ttu-id="f9996-108">[in] Handle to the error value generated in the previous method call.</span><span class="sxs-lookup"><span data-stu-id="f9996-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="f9996-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9996-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f9996-110">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f9996-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f9996-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f9996-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f9996-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9996-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f9996-113">Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="f9996-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f9996-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f9996-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f9996-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f9996-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f9996-116">[out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="f9996-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f9996-117">Для  _параметра lppMAPIError_ можно установить NULL, если поставщик не может предоставить структуру **MAPIERROR** с соответствующей информацией.</span><span class="sxs-lookup"><span data-stu-id="f9996-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f9996-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9996-118">Return value</span></span>

<span data-ttu-id="f9996-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9996-119">S_OK</span></span> 
  
> <span data-ttu-id="f9996-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f9996-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f9996-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f9996-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f9996-122">Либо флаг MAPI_UNICODE установлен, а поставщик адресной книги не поддерживает Юникод, либо MAPI_UNICODE не установлен, а поставщик адресной книги поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f9996-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9996-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9996-123">Remarks</span></span>

<span data-ttu-id="f9996-124">Поставщики адресных книг реализуют метод **GetLastError** для получения сведений о вызове предыдущего метода, который не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="f9996-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="f9996-125">Вызыватели могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f9996-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9996-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f9996-126">Notes to callers</span></span>

<span data-ttu-id="f9996-127">Можно использовать структуру **MAPIERROR,** на которую указывает параметр  _lppMAPIError,_ если поставщик адресной книги передает структуру и только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="f9996-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="f9996-128">Иногда поставщик адресной книги не может определить, какая была последняя ошибка, или больше не имеет данных для отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f9996-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="f9996-129">В этой ситуации поставщик адресной книги возвращает указатель на NULL в _lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="f9996-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="f9996-130">Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="f9996-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9996-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f9996-131">See also</span></span>



[<span data-ttu-id="f9996-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f9996-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f9996-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9996-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f9996-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9996-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

