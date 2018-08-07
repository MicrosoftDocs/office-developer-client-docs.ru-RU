---
title: SCODE
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
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812204"
---
# <a name="scode"></a><span data-ttu-id="183a2-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="183a2-103">SCODE</span></span>

<span data-ttu-id="183a2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="183a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="183a2-105">Значение состояния 32-разрядная версия, используемый для описания сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="183a2-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="183a2-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="183a2-106">Remarks</span></span>

<span data-ttu-id="183a2-107">Тип данных **SCODE** — то же, что тип данных [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="183a2-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="183a2-108">Значение **SCODE** делится на четыре поля:</span><span class="sxs-lookup"><span data-stu-id="183a2-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="183a2-109">Уровень серьезности незначительно код, который имеет значение 0 для обозначения успешности и 1 при сбое.</span><span class="sxs-lookup"><span data-stu-id="183a2-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="183a2-110">Это поле зарезервировано 11-разрядная версия</span><span class="sxs-lookup"><span data-stu-id="183a2-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="183a2-111">4-разрядное оборудование код, который определяет область, ответственный за сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="183a2-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="183a2-112">16-разрядный ошибку или предупреждение кода, который описывает проблему, которая вызывает ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="183a2-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="183a2-113">Многие из функций MAPI и методов возвращаемые значения **SCODE** определен как типы данных **HRESULT** , как выполнить OLE методы и функции.</span><span class="sxs-lookup"><span data-stu-id="183a2-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="183a2-114">OLE определяет несколько макросов, которые можно использовать для преобразования между **SCODE** и значение **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="183a2-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="183a2-115">В 64-разрядная версия MAPI **SCODE** по-прежнему значение 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="183a2-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="183a2-116">Дополнительные сведения об использовании MAPI тип данных **SCODE** можно [Обработки ошибок](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="183a2-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="183a2-117">Дополнительные сведения о OLE и тип данных **SCODE** *OLE Справочник программиста* см.</span><span class="sxs-lookup"><span data-stu-id="183a2-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="183a2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="183a2-118">See also</span></span>



[<span data-ttu-id="183a2-119">HRESULT</span><span class="sxs-lookup"><span data-stu-id="183a2-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="183a2-120">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="183a2-120">MAPI Data Types</span></span>](mapi-data-types.md)

