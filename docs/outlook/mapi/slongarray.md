---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414531"
---
# <a name="slongarray"></a><span data-ttu-id="3e981-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="3e981-103">SLongArray</span></span>

  
  
<span data-ttu-id="3e981-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e981-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e981-105">Содержит массив типов ДЛИННых значений, которые используются для описания свойства типа ПТ_МВ_ЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="3e981-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e981-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3e981-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e981-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3e981-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="3e981-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e981-108">Members</span></span>

 <span data-ttu-id="3e981-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="3e981-109">**cValues**</span></span>
  
> <span data-ttu-id="3e981-110">Количество значений в массиве, на которое указывает элемент **ЛПЛ** .</span><span class="sxs-lookup"><span data-stu-id="3e981-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="3e981-111">**ЛПЛ**</span><span class="sxs-lookup"><span data-stu-id="3e981-111">**lpl**</span></span>
  
> <span data-ttu-id="3e981-112">Указатель на массив ДЛИННых значений.</span><span class="sxs-lookup"><span data-stu-id="3e981-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e981-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e981-113">Remarks</span></span>

<span data-ttu-id="3e981-114">Дополнительные сведения о ПТ_МВ_ЛОНГ приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3e981-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e981-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3e981-115">See also</span></span>



[<span data-ttu-id="3e981-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3e981-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3e981-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3e981-117">MAPI Structures</span></span>](mapi-structures.md)

