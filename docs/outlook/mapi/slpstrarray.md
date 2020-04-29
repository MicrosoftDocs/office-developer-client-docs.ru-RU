---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435910"
---
# <a name="slpstrarray"></a><span data-ttu-id="28346-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="28346-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="28346-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28346-105">Содержит массив строковых значений, которые используются для описания свойства типа PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="28346-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28346-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="28346-106">Header file:</span></span>  <br/> |<span data-ttu-id="28346-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="28346-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="28346-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="28346-108">Members</span></span>

 <span data-ttu-id="28346-109">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="28346-109">**cValues**</span></span>
  
> <span data-ttu-id="28346-110">Количество значений в массиве, на которое указывает элемент **лппсза** .</span><span class="sxs-lookup"><span data-stu-id="28346-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="28346-111">**лппсза**</span><span class="sxs-lookup"><span data-stu-id="28346-111">**lppszA**</span></span>
  
> <span data-ttu-id="28346-112">Указатель на массив 8 – разрядных символьных строк со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="28346-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28346-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="28346-113">Remarks</span></span>

<span data-ttu-id="28346-114">Дополнительные сведения о PT_MV_STRING8 приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="28346-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28346-115">См. также</span><span class="sxs-lookup"><span data-stu-id="28346-115">See also</span></span>



[<span data-ttu-id="28346-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="28346-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="28346-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="28346-117">MAPI Structures</span></span>](mapi-structures.md)

