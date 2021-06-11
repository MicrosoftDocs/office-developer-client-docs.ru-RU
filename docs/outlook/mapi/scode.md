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
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430135"
---
# <a name="scode"></a><span data-ttu-id="ecafa-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="ecafa-103">SCODE</span></span>

<span data-ttu-id="ecafa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecafa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecafa-105">32-битное значение состояния, которое используется для описания ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ecafa-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="ecafa-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecafa-106">Remarks</span></span>

<span data-ttu-id="ecafa-107">Тип **данных SCODE** такой же, как и [тип данных HRESULT.](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="ecafa-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="ecafa-108">Значение **SCODE** разделено на четыре поля:</span><span class="sxs-lookup"><span data-stu-id="ecafa-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="ecafa-109">Одно-разрядный код серьезности, который указывает на успешность, а 1 — на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ecafa-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="ecafa-110">11-битное зарезервированное поле</span><span class="sxs-lookup"><span data-stu-id="ecafa-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="ecafa-111">4-битный код объекта, который указывает область, ответственную за ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="ecafa-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="ecafa-112">16-битный код ошибки или предупреждения, описывающий проблему, вызываемую ошибкой или предупреждением.</span><span class="sxs-lookup"><span data-stu-id="ecafa-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="ecafa-113">Многие функции и методы MAPI возвращают **значения SCODE,** определенные как типы данных **HRESULT,** как и методы и функции OLE.</span><span class="sxs-lookup"><span data-stu-id="ecafa-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="ecafa-114">OLE определяет несколько макрос, которые можно использовать для преобразования между **SCODE** и **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ecafa-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ecafa-115">В 64-битной MAPI **SCODE** по-прежнему является 32-битным значением.</span><span class="sxs-lookup"><span data-stu-id="ecafa-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="ecafa-116">Дополнительные сведения о том, как MAPI использует **тип данных SCODE,** см. в сообщении [Об обработке ошибок.](error-handling-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="ecafa-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="ecafa-117">Дополнительные сведения о OLE и **типе данных SCODE** см. в справке к *программисту OLE.*</span><span class="sxs-lookup"><span data-stu-id="ecafa-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecafa-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ecafa-118">See also</span></span>



[<span data-ttu-id="ecafa-119">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ecafa-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="ecafa-120">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="ecafa-120">MAPI Data Types</span></span>](mapi-data-types.md)

