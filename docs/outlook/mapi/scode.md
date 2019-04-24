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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351242"
---
# <a name="scode"></a><span data-ttu-id="9e294-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="9e294-103">SCODE</span></span>

<span data-ttu-id="9e294-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e294-105">32-разрядное значение состояния, используемое для описания ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9e294-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="9e294-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e294-106">Remarks</span></span>

<span data-ttu-id="9e294-107">Тип данных **SCODE** такой же, как и тип данных [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="9e294-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="9e294-108">Значение **SCODE** разделено на четыре поля:</span><span class="sxs-lookup"><span data-stu-id="9e294-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="9e294-109">Одноразрядный код серьезности, который имеет значение 0 для обозначения успеха и 1 для обозначения сбоя.</span><span class="sxs-lookup"><span data-stu-id="9e294-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="9e294-110">11 – битовое зарезервированное поле</span><span class="sxs-lookup"><span data-stu-id="9e294-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="9e294-111">4 разрядный код средства, указывающий область, отвечающую за сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="9e294-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="9e294-112">16-разрядный код ошибки или предупреждения, описывающий проблему, которая вызывает ошибку или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="9e294-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="9e294-113">Многие функции и методы MAPI возвращают значения **SCODE** , определенные как типы данных **HRESULT** как методы и функции OLE.</span><span class="sxs-lookup"><span data-stu-id="9e294-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="9e294-114">OLE определяет несколько макросов, которые можно использовать для преобразования между **SCODE** и **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e294-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9e294-115">В 64-бит MAPI **SCODE** по-прежнему является 32-битным значением.</span><span class="sxs-lookup"><span data-stu-id="9e294-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="9e294-116">Дополнительные сведения о том, как MAPI использует тип данных **SCODE** , можно узнать в статье [Обработка ошибок](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="9e294-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="9e294-117">Дополнительные сведения о OLE и типе данных **SCODE** можно найти в справочном *справочнике по OLE программисту* .</span><span class="sxs-lookup"><span data-stu-id="9e294-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e294-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9e294-118">See also</span></span>



[<span data-ttu-id="9e294-119">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e294-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="9e294-120">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="9e294-120">MAPI Data Types</span></span>](mapi-data-types.md)

