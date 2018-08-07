---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808659"
---
# <a name="hresult"></a><span data-ttu-id="92b5c-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="92b5c-103">HRESULT</span></span>

  
  
<span data-ttu-id="92b5c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92b5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92b5c-105">Значение 32-разрядная версия, используемый для описания сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="92b5c-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="92b5c-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="92b5c-106">Remarks</span></span>

<span data-ttu-id="92b5c-107">Тип данных **HRESULT** — то же, что тип данных [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="92b5c-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="92b5c-108">Значение **HRESULT** состоит из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="92b5c-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="92b5c-109">1-разрядный код, указывающий уровень серьезности, где нулевой представляет успеха и 1 представляет сбоя.</span><span class="sxs-lookup"><span data-stu-id="92b5c-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="92b5c-110">4-битное значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="92b5c-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="92b5c-111">11-разрядный код, указывающее ответственность за сообщение об ошибке или предупреждение, также известной как код средства.</span><span class="sxs-lookup"><span data-stu-id="92b5c-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="92b5c-112">16-разрядный код, описывающее ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="92b5c-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="92b5c-113">Большинство методов интерфейса MAPI и функции, возвращаемые значения **HRESULT** для предоставления подробные причина возникновения.</span><span class="sxs-lookup"><span data-stu-id="92b5c-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="92b5c-114">Значения **HRESULT** также получила широкого применения в методы интерфейса OLE.</span><span class="sxs-lookup"><span data-stu-id="92b5c-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="92b5c-115">OLE предоставляет несколько макросов для преобразования значения **HRESULT** и значения **SCODE** введите другой общих данных для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="92b5c-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="92b5c-116">В 64-разрядная версия MAPI **HRESULT** по-прежнему значение 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="92b5c-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="92b5c-117">Дополнительные сведения об использовании OLE значения **HRESULT** видеть *OLE Справочник программиста* .</span><span class="sxs-lookup"><span data-stu-id="92b5c-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="92b5c-118">Дополнительные сведения об использовании этих значений в MAPI можно [Обработки ошибок](error-handling-in-mapi.md) и какие-либо из следующих методов интерфейса:</span><span class="sxs-lookup"><span data-stu-id="92b5c-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="92b5c-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92b5c-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="92b5c-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92b5c-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="92b5c-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92b5c-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="92b5c-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92b5c-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="92b5c-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92b5c-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="92b5c-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="92b5c-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="92b5c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="92b5c-125">See also</span></span>



[<span data-ttu-id="92b5c-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="92b5c-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="92b5c-127">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="92b5c-127">MAPI Data Types</span></span>](mapi-data-types.md)

