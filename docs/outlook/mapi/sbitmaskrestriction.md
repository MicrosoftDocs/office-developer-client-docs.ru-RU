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
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424478"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="bc04b-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="bc04b-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="bc04b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc04b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc04b-105">Описывает ограничение bitmask, которое используется для выполнения немного пошаговых действий **и** проверки результата.</span><span class="sxs-lookup"><span data-stu-id="bc04b-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc04b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bc04b-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc04b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc04b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="bc04b-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="bc04b-108">Members</span></span>

 <span data-ttu-id="bc04b-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="bc04b-109">**relBMR**</span></span>
  
> <span data-ttu-id="bc04b-110">Реляционный оператор, описывая, как маска, указанная в члене **ulMask,** должна применяться к тегу свойства.</span><span class="sxs-lookup"><span data-stu-id="bc04b-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="bc04b-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="bc04b-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="bc04b-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="bc04b-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="bc04b-113">Выполните немного  и операция маски в **члене ulMask** с свойством, представленным членом **ulPropTag,** и проверьте, как быть равным нулю.</span><span class="sxs-lookup"><span data-stu-id="bc04b-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="bc04b-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="bc04b-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="bc04b-115">Выполните немного  и операция маски в **члене ulMask** с свойством, представленным членом **ulPropTag,** и проверьте, что значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bc04b-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="bc04b-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="bc04b-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="bc04b-117">Тег свойства свойства, к которому применяется битмаска.</span><span class="sxs-lookup"><span data-stu-id="bc04b-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="bc04b-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="bc04b-118">**ulMask**</span></span>
  
> <span data-ttu-id="bc04b-119">Bitmask для применения к свойству, идентифицированного **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="bc04b-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc04b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc04b-120">Remarks</span></span>

<span data-ttu-id="bc04b-121">Структура **SBitMaskRestriction** выполняет немного  и выполняет операцию с помощью битмаски, описанной в члене **ulMask,** и значения свойства, описанного участником **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="bc04b-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="bc04b-122">Если результат нулевой, BMR_EQZ удовлетворены.</span><span class="sxs-lookup"><span data-stu-id="bc04b-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="bc04b-123">Если оно незеро, то есть если значение свойства имеет по крайней мере один из тех же битов, что и **ulMask,** BMR_NEZ удовлетворены.</span><span class="sxs-lookup"><span data-stu-id="bc04b-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="bc04b-124">Дополнительные сведения о структуре **sBitMaskRestriction** и ограничениях в целом см. в [рубрике Ограничения.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="bc04b-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc04b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bc04b-125">See also</span></span>



[<span data-ttu-id="bc04b-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bc04b-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="bc04b-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bc04b-127">MAPI Structures</span></span>](mapi-structures.md)

