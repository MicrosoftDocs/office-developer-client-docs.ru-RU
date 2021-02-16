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
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435021"
---
# <a name="hresult"></a><span data-ttu-id="7975a-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7975a-103">HRESULT</span></span>

  
  
<span data-ttu-id="7975a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7975a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7975a-105">32-битное значение, которое используется для описания ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7975a-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="7975a-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="7975a-106">Remarks</span></span>

<span data-ttu-id="7975a-107">Тип **данных HRESULT** такой же, как и тип [данных SCODE.](scode.md)</span><span class="sxs-lookup"><span data-stu-id="7975a-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="7975a-108">Значение **HRESULT** состоит из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="7975a-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="7975a-109">1-битный код, указывающий серьезность, где ноль означает успех, а 1 — сбой.</span><span class="sxs-lookup"><span data-stu-id="7975a-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="7975a-110">4-битное зарезервированное значение.</span><span class="sxs-lookup"><span data-stu-id="7975a-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="7975a-111">11-битный код, указывающий ответственность за ошибку или предупреждение, также известный как код объекта.</span><span class="sxs-lookup"><span data-stu-id="7975a-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="7975a-112">16-битный код, описывающий ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="7975a-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="7975a-113">Большинство методов и функций интерфейса MAPI возвращают **значения HRESULT,** чтобы предоставить подробные сведения о причинах.</span><span class="sxs-lookup"><span data-stu-id="7975a-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="7975a-114">**Значения HRESULT** также широко используются в методах интерфейса OLE.</span><span class="sxs-lookup"><span data-stu-id="7975a-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="7975a-115">OLE предоставляет несколько макроса для преобразования значений **HRESULT** в **значения SCODE,** еще один распространенный тип данных для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="7975a-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7975a-116">В 64-битных MAPI **HRESULT** по-прежнему является 32-битным значением.</span><span class="sxs-lookup"><span data-stu-id="7975a-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="7975a-117">Сведения об использовании значений **HRESULT** в OLE см. в справочнике *по OLE Programmer.*</span><span class="sxs-lookup"><span data-stu-id="7975a-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="7975a-118">Дополнительные сведения об использовании этих значений в [](error-handling-in-mapi.md) MAPI см. в обработке ошибок и любом из следующих методов интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7975a-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="7975a-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7975a-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="7975a-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7975a-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="7975a-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7975a-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="7975a-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7975a-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="7975a-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7975a-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="7975a-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="7975a-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="7975a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7975a-125">See also</span></span>



[<span data-ttu-id="7975a-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="7975a-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="7975a-127">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="7975a-127">MAPI Data Types</span></span>](mapi-data-types.md)

