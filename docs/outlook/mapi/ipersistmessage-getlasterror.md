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
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="caa59-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="caa59-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="caa59-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caa59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caa59-105">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="caa59-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="caa59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caa59-106">Parameters</span></span>

 <span data-ttu-id="caa59-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="caa59-107">_hResult_</span></span>
  
> <span data-ttu-id="caa59-108">[in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="caa59-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="caa59-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="caa59-109">_ulFlags_</span></span>
  
> <span data-ttu-id="caa59-110">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="caa59-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="caa59-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="caa59-111">The following flag can be set:</span></span>
    
<span data-ttu-id="caa59-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="caa59-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="caa59-113">Строки в структуре [MAPIERROR,](mapierror.md) возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="caa59-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="caa59-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="caa59-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="caa59-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="caa59-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="caa59-116">[out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="caa59-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="caa59-117">Для _параметра lppMAPIError_ можно установить NULL, если форма не может предоставить соответствующие сведения для структуры **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="caa59-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="caa59-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caa59-118">Return value</span></span>

<span data-ttu-id="caa59-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="caa59-119">S_OK</span></span> 
  
> <span data-ttu-id="caa59-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="caa59-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="caa59-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="caa59-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="caa59-122">Либо флаг MAPI_UNICODE установлен, а поставщик адресной книги не поддерживает Юникод, либо MAPI_UNICODE не установлен, а поставщик адресной книги поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="caa59-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caa59-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="caa59-123">Remarks</span></span>

<span data-ttu-id="caa59-124">Объекты форм реализуют метод **IPersistMessage::GetLastError** для получения сведений о предыдущем вызове метода, который не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="caa59-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="caa59-125">Посетители форм могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="caa59-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="caa59-126">Вызов **GetLastError** не влияет на состояние формы.</span><span class="sxs-lookup"><span data-stu-id="caa59-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="caa59-127">При **возвращении GetLastError** форма остается в состоянии, в которое она была до вызова.</span><span class="sxs-lookup"><span data-stu-id="caa59-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="caa59-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="caa59-128">Notes to callers</span></span>

<span data-ttu-id="caa59-129">Можно использовать структуру **MAPIERROR,** если форма указывает на нее, на которую указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="caa59-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="caa59-130">Иногда форма не может определить, какая была последняя ошибка, или больше не имеет для отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="caa59-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="caa59-131">В этой ситуации форма возвращает указатель на NULL в _lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="caa59-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="caa59-132">Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="caa59-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="caa59-133">См. также</span><span class="sxs-lookup"><span data-stu-id="caa59-133">See also</span></span>



[<span data-ttu-id="caa59-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="caa59-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="caa59-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="caa59-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="caa59-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="caa59-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

