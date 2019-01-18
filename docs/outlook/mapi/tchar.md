---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710449"
---
# <a name="tchar"></a><span data-ttu-id="b5824-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="b5824-103">TCHAR</span></span>

  
  
<span data-ttu-id="b5824-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5824-p101">Строка символов Win32, которая позволяет описать строки Юникода, ANSI или DBCS. Для платформ ANSI и DBCS TCHAR определяется так:</span><span class="sxs-lookup"><span data-stu-id="b5824-p101">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings. For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="b5824-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5824-107">Remarks</span></span>

<span data-ttu-id="b5824-108">Для платформ Юникод TCHAR определяется как синоним типа WCHAR.</span><span class="sxs-lookup"><span data-stu-id="b5824-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="b5824-p102">Клиенты MAPI могут использовать тип данных TCHAR для представления строки типа char или WCHAR. Определите символьную константу UNICODE и ограничьте платформу при необходимости. MAPI интерпретирует данные платформы и внутренне преобразует TCHAR в соответствующую строку. Тип свойства MAPI, PT_TSTRING, работает так же, как и тип данных TCHAR. Если платформа поддерживает Юникод, свойствам типа PT_TSTRING назначается тип PT_UNICODE во время компиляции. Если платформа не поддерживает Юникод, этим свойствам назначается тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="b5824-p102">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type. Be sure to define the symbolic constant UNICODE and limit the platform when it is required. MAPI will interpret the platform information and internally translate TCHAR to the appropriate string. The MAPI property type, PT_TSTRING, works just like the TCHAR data type. When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time. When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="b5824-115">Чтобы узнать больше об этой функции, просмотрите [кодировки](mapi-character-sets.md) и [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b5824-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5824-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b5824-116">See also</span></span>



[<span data-ttu-id="b5824-117">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="b5824-117">MAPI Data Types</span></span>](mapi-data-types.md)

