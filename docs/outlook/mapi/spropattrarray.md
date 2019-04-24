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
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358116"
---
# <a name="spropattrarray"></a><span data-ttu-id="cd192-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cd192-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="cd192-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd192-105">Содержит список атрибутов для свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="cd192-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd192-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cd192-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd192-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="cd192-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="cd192-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="cd192-108">Related macros:</span></span>  <br/> |<span data-ttu-id="cd192-109">[Кбневспропаттраррай](cbnewspropattrarray.md), [кбспропаттраррай](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="cd192-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="cd192-110">Members</span><span class="sxs-lookup"><span data-stu-id="cd192-110">Members</span></span>

 <span data-ttu-id="cd192-111">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="cd192-111">**cValues**</span></span>
  
> <span data-ttu-id="cd192-112">Количество атрибутов свойств в элементе **апропаттр** .</span><span class="sxs-lookup"><span data-stu-id="cd192-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="cd192-113">**Апропаттр**</span><span class="sxs-lookup"><span data-stu-id="cd192-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="cd192-114">Массив атрибутов свойств.</span><span class="sxs-lookup"><span data-stu-id="cd192-114">An array of property attributes.</span></span> <span data-ttu-id="cd192-115">Для атрибутов допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cd192-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="cd192-116">ПРОПАТТР_МАНДАТОРИ</span><span class="sxs-lookup"><span data-stu-id="cd192-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="cd192-117">ПРОПАТТР_РЕАДАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="cd192-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="cd192-118">ПРОПАТТР_ВРИТЕАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="cd192-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="cd192-119">ПРОПАТТР_НОТ_ПРЕСЕНТ</span><span class="sxs-lookup"><span data-stu-id="cd192-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd192-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd192-120">Remarks</span></span>

<span data-ttu-id="cd192-121">Структура **спропаттраррай** используется объектами данных свойств, которые реализуют интерфейс [ипропдата: IMAPIProp](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="cd192-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="cd192-122">Он также используется реализацией интерфейса MAPI [имапимессажесите: IUnknown](imapimessagesiteiunknown.md) , основанного на структурированном хранилище.</span><span class="sxs-lookup"><span data-stu-id="cd192-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd192-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cd192-123">See also</span></span>



[<span data-ttu-id="cd192-124">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cd192-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="cd192-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd192-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="cd192-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cd192-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="cd192-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cd192-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="cd192-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="cd192-128">MAPI Structures</span></span>](mapi-structures.md)

