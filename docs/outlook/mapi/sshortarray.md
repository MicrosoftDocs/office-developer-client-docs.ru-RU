---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429616"
---
# <a name="sshortarray"></a><span data-ttu-id="22609-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="22609-103">SShortArray</span></span>

  
  
<span data-ttu-id="22609-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22609-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22609-105">Содержит массив неподписаенных целый значений, используемых для описания свойства типа PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="22609-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22609-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="22609-106">Header file:</span></span>  <br/> |<span data-ttu-id="22609-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22609-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="22609-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="22609-108">Members</span></span>

 <span data-ttu-id="22609-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="22609-109">**cValues**</span></span>
  
> <span data-ttu-id="22609-110">Количество значений в массиве, на который указывает член **LPI.**</span><span class="sxs-lookup"><span data-stu-id="22609-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="22609-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="22609-111">**lpi**</span></span>
  
> <span data-ttu-id="22609-112">Указатель на массив неподписаных значений.</span><span class="sxs-lookup"><span data-stu-id="22609-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22609-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="22609-113">Remarks</span></span>

<span data-ttu-id="22609-114">Дополнительные сведения о типах PT_MV_SHORT и других типах свойств см. [в подгонах "Типы свойств".](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="22609-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22609-115">См. также</span><span class="sxs-lookup"><span data-stu-id="22609-115">See also</span></span>



[<span data-ttu-id="22609-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="22609-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="22609-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="22609-117">MAPI Structures</span></span>](mapi-structures.md)

