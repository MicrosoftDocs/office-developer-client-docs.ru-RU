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
# <a name="hresult"></a><span data-ttu-id="75bfc-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="75bfc-103">HRESULT</span></span>

  
  
<span data-ttu-id="75bfc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75bfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75bfc-105">32-битное значение, которое используется для описания ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="75bfc-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="75bfc-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="75bfc-106">Remarks</span></span>

<span data-ttu-id="75bfc-107">Тип **данных HRESULT** такой же, как и [тип данных SCODE.](scode.md)</span><span class="sxs-lookup"><span data-stu-id="75bfc-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="75bfc-108">Значение **HRESULT** состоит из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="75bfc-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="75bfc-109">1-битный код, указывающий серьезность, где ноль представляет успех, а 1 — сбой.</span><span class="sxs-lookup"><span data-stu-id="75bfc-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="75bfc-110">4-битное зарезервированное значение.</span><span class="sxs-lookup"><span data-stu-id="75bfc-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="75bfc-111">11-битный код, указывающий ответственность за ошибку или предупреждение, также известный как код объекта.</span><span class="sxs-lookup"><span data-stu-id="75bfc-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="75bfc-112">16-битный код, описывающий ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="75bfc-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="75bfc-113">Большинство методов и функций интерфейса MAPI возвращают **значения HRESULT,** чтобы обеспечить подробное формирование причин.</span><span class="sxs-lookup"><span data-stu-id="75bfc-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="75bfc-114">**Значения HRESULT** также широко используются в методах интерфейса OLE.</span><span class="sxs-lookup"><span data-stu-id="75bfc-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="75bfc-115">OLE предоставляет несколько макрос для преобразования между **значениями HRESULT** и **SCODE,** другим распространенным типом данных для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="75bfc-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="75bfc-116">В 64-битной MAPI **значение HRESULT** по-прежнему равно 32-битным значениям.</span><span class="sxs-lookup"><span data-stu-id="75bfc-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="75bfc-117">Сведения об использовании значений **HRESULT** в OLE см. в справке к *программисту OLE.*</span><span class="sxs-lookup"><span data-stu-id="75bfc-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="75bfc-118">Дополнительные сведения об использовании этих значений в MAPI см. в примере [Обработка](error-handling-in-mapi.md) ошибок и любой из следующих методов интерфейса:</span><span class="sxs-lookup"><span data-stu-id="75bfc-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="75bfc-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="75bfc-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="75bfc-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="75bfc-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="75bfc-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="75bfc-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="75bfc-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="75bfc-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="75bfc-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="75bfc-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="75bfc-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="75bfc-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="75bfc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="75bfc-125">See also</span></span>



[<span data-ttu-id="75bfc-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="75bfc-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="75bfc-127">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="75bfc-127">MAPI Data Types</span></span>](mapi-data-types.md)

