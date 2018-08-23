---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9197201388530bd7755eb1987ecc863220e3847
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566609"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="5aad5-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="5aad5-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="5aad5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5aad5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5aad5-105">Описание ограничений Битовая маска, которая используется для выполнения побитовую операцию **и** и проверять этот результат.</span><span class="sxs-lookup"><span data-stu-id="5aad5-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5aad5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5aad5-106">Header file:</span></span>  <br/> |<span data-ttu-id="5aad5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5aad5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="5aad5-108">Members</span><span class="sxs-lookup"><span data-stu-id="5aad5-108">Members</span></span>

 <span data-ttu-id="5aad5-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="5aad5-109">**relBMR**</span></span>
  
> <span data-ttu-id="5aad5-110">Оператор сравнения, описывающая способ применения маска, указанных в член **ulMask** тега свойства.</span><span class="sxs-lookup"><span data-stu-id="5aad5-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="5aad5-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="5aad5-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="5aad5-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="5aad5-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="5aad5-113">Выполните операцию побитовое **и** маски в член **ulMask** со свойством, представленных член **ulPropTag** и тестирования, равное нулю.</span><span class="sxs-lookup"><span data-stu-id="5aad5-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="5aad5-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="5aad5-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="5aad5-115">Выполните операцию побитовое **и** маски в член **ulMask** со свойством, представленное член **ulPropTag** и проверить, не равное нулю.</span><span class="sxs-lookup"><span data-stu-id="5aad5-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="5aad5-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5aad5-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="5aad5-117">Свойство tag свойства, к которому применяется Битовая маска.</span><span class="sxs-lookup"><span data-stu-id="5aad5-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="5aad5-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="5aad5-118">**ulMask**</span></span>
  
> <span data-ttu-id="5aad5-119">Битовую маску, применяемую к свойству, определяемую средством **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="5aad5-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5aad5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="5aad5-120">Remarks</span></span>

<span data-ttu-id="5aad5-121">Структура **SBitMaskRestriction** выполняет побитовое операцию **и** с помощью Битовая маска, описанные в член **ulMask** и значение свойства, описанные член **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="5aad5-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="5aad5-122">Если значение равно нулю, выполняется BMR_EQZ.</span><span class="sxs-lookup"><span data-stu-id="5aad5-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="5aad5-123">Если ненулевое значение, то есть, если значение свойства есть по крайней мере один из того же битов задаются в виде **ulMask**, затем BMR_NEZ выполняется.</span><span class="sxs-lookup"><span data-stu-id="5aad5-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="5aad5-124">Дополнительные сведения о структуре **SBitMaskRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5aad5-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5aad5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5aad5-125">See also</span></span>



[<span data-ttu-id="5aad5-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5aad5-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="5aad5-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5aad5-127">MAPI Structures</span></span>](mapi-structures.md)

