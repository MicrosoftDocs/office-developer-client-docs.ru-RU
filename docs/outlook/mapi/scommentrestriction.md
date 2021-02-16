---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430611"
---
# <a name="scommentrestriction"></a><span data-ttu-id="1631d-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="1631d-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="1631d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1631d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1631d-105">Описывает ограничение комментария, которое используется для примечать к ограничению.</span><span class="sxs-lookup"><span data-stu-id="1631d-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1631d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1631d-106">Header file:</span></span>  <br/> |<span data-ttu-id="1631d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1631d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="1631d-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="1631d-108">Members</span></span>

 <span data-ttu-id="1631d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1631d-109">**cValues**</span></span>
  
> <span data-ttu-id="1631d-110">Количество значений свойств в массиве, на который указывает **член lpProp.**</span><span class="sxs-lookup"><span data-stu-id="1631d-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="1631d-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="1631d-111">**lpRes**</span></span>
  
> <span data-ttu-id="1631d-112">Указатель на [структуру SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="1631d-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="1631d-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="1631d-113">**lpProp**</span></span>
  
> <span data-ttu-id="1631d-114">Указатель на массив структур [SPropValue,](spropvalue.md) каждый из которых содержит тег свойства и значение для именоваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1631d-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1631d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1631d-115">Remarks</span></span>

<span data-ttu-id="1631d-116">Структура **SCommentRestriction** связывает объект с набором именуемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1631d-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="1631d-117">Ограничения комментариев не являются другими ограничениями, так как они не оцениваются.</span><span class="sxs-lookup"><span data-stu-id="1631d-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="1631d-118">То есть они игнорируются методом [IMAPITable::Restrict.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="1631d-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="1631d-119">После вызова **IMAPITable::Restrict** строки, возвращаемые методом [IMAPITable::QueryRows,](imapitable-queryrows.md) не влияют.</span><span class="sxs-lookup"><span data-stu-id="1631d-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="1631d-120">Структуру **SCommentRestriction** можно использовать для сохраняемой на диске информации для конкретного приложения с ограничением.</span><span class="sxs-lookup"><span data-stu-id="1631d-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="1631d-121">Например, клиент, с сохранением имени именоваемого свойства, используемого в ограничении свойств, может сделать это в структуре **SCommentRestriction.**</span><span class="sxs-lookup"><span data-stu-id="1631d-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="1631d-122">Сохранение имени свойства невозможно в ограничении свойства, так как связанная [структура SPropertyRestriction](spropertyrestriction.md) содержит только тег свойства.</span><span class="sxs-lookup"><span data-stu-id="1631d-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="1631d-123">Дополнительные сведения о структуре **и ограничениях SCommentRestriction** в целом см. в сведениях [об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="1631d-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1631d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1631d-124">See also</span></span>



[<span data-ttu-id="1631d-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1631d-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1631d-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="1631d-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="1631d-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="1631d-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="1631d-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1631d-128">MAPI Structures</span></span>](mapi-structures.md)

