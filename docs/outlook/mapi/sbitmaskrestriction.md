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
# <a name="sbitmaskrestriction"></a><span data-ttu-id="6655b-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="6655b-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="6655b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6655b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6655b-105">Описывает ограничение битовой маски, которое используется для выполнения поразрядной операции **and** и проверки результата.</span><span class="sxs-lookup"><span data-stu-id="6655b-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6655b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6655b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6655b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6655b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="6655b-108">Members</span><span class="sxs-lookup"><span data-stu-id="6655b-108">Members</span></span>

 <span data-ttu-id="6655b-109">**Релбмр**</span><span class="sxs-lookup"><span data-stu-id="6655b-109">**relBMR**</span></span>
  
> <span data-ttu-id="6655b-110">Оператор отношения, описывающий, как маска, указанная в элементе **улмаск** , должна быть применена к тегу свойства.</span><span class="sxs-lookup"><span data-stu-id="6655b-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="6655b-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6655b-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="6655b-112">БМР_ЕКЗ</span><span class="sxs-lookup"><span data-stu-id="6655b-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="6655b-113">Выполните побитовую операцию **and** для маски в элементе **улмаск** со свойством, представленным элементом **улпроптаг** , и протестируйте его равным нулю.</span><span class="sxs-lookup"><span data-stu-id="6655b-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="6655b-114">БМР_НЕЗ</span><span class="sxs-lookup"><span data-stu-id="6655b-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="6655b-115">Выполните побитовую операцию **and** для маски в элементе **улмаск** со свойством, представленным элементом **улпроптаг** , и проверьте, что оно не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6655b-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="6655b-116">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="6655b-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="6655b-117">Тег свойства свойства, к которому применяется битовая маска.</span><span class="sxs-lookup"><span data-stu-id="6655b-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="6655b-118">**Улмаск**</span><span class="sxs-lookup"><span data-stu-id="6655b-118">**ulMask**</span></span>
  
> <span data-ttu-id="6655b-119">Битовая маска, применяемая к свойству, определенному с помощью **улпроптаг**.</span><span class="sxs-lookup"><span data-stu-id="6655b-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6655b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="6655b-120">Remarks</span></span>

<span data-ttu-id="6655b-121">Структура **сбитмаскрестриктион** выполняет битовую операцию **и** использует битовую маску, описанную в элементе **улмаск** , и значение свойства, описываемого элементом **улпроптаг** .</span><span class="sxs-lookup"><span data-stu-id="6655b-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="6655b-122">Если результат равен нулю, БМР_ЕКЗ является удовлетворенным.</span><span class="sxs-lookup"><span data-stu-id="6655b-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="6655b-123">Если это ненулевое значение, то есть, если значение свойства имеет по крайней мере один такой же бит, что и **улмаск**, то бмр_нез является удовлетворенным.</span><span class="sxs-lookup"><span data-stu-id="6655b-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="6655b-124">Для получения дополнительных сведений о структуре и ограничениях **сбитмаскрестриктион** в целом ознакомьтесь [](about-restrictions.md)с ограничениями.</span><span class="sxs-lookup"><span data-stu-id="6655b-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6655b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6655b-125">See also</span></span>



[<span data-ttu-id="6655b-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="6655b-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="6655b-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6655b-127">MAPI Structures</span></span>](mapi-structures.md)

