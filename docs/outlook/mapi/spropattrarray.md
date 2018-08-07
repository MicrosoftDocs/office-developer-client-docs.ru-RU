---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812362"
---
# <a name="spropattrarray"></a><span data-ttu-id="e42c9-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="e42c9-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="e42c9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e42c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e42c9-105">Содержит список атрибутов для свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="e42c9-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e42c9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e42c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="e42c9-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="e42c9-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e42c9-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="e42c9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="e42c9-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="e42c9-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="e42c9-110">Members</span><span class="sxs-lookup"><span data-stu-id="e42c9-110">Members</span></span>

 <span data-ttu-id="e42c9-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e42c9-111">**cValues**</span></span>
  
> <span data-ttu-id="e42c9-112">Число свойств атрибуты в элемент **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="e42c9-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="e42c9-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="e42c9-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="e42c9-114">Массив атрибутов свойств.</span><span class="sxs-lookup"><span data-stu-id="e42c9-114">An array of property attributes.</span></span> <span data-ttu-id="e42c9-115">Допустимые значения для атрибутов, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e42c9-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="e42c9-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="e42c9-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="e42c9-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="e42c9-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="e42c9-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="e42c9-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="e42c9-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="e42c9-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e42c9-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="e42c9-120">Remarks</span></span>

<span data-ttu-id="e42c9-121">Структура **SPropAttrArray** используется объектами данных свойств, которые реализуют [IPropData: IMAPIProp](ipropdataimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e42c9-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="e42c9-122">Он также используется в реализации интерфейса MAPI [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) то есть на основе структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e42c9-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e42c9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e42c9-123">See also</span></span>



[<span data-ttu-id="e42c9-124">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e42c9-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="e42c9-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e42c9-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="e42c9-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="e42c9-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="e42c9-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="e42c9-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="e42c9-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e42c9-128">MAPI Structures</span></span>](mapi-structures.md)

