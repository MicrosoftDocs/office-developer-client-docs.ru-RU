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
ms.openlocfilehash: 2185b059f2b831a14b90bad3a3c286ed72f8234d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812203"
---
# <a name="scommentrestriction"></a><span data-ttu-id="51896-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="51896-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="51896-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51896-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51896-105">Описание ограничений комментарий, который используется для аннотирования ограничение.</span><span class="sxs-lookup"><span data-stu-id="51896-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51896-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="51896-106">Header file:</span></span>  <br/> |<span data-ttu-id="51896-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51896-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="51896-108">Members</span><span class="sxs-lookup"><span data-stu-id="51896-108">Members</span></span>

 <span data-ttu-id="51896-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="51896-109">**cValues**</span></span>
  
> <span data-ttu-id="51896-110">Число значений свойств в массиве, на который указывает член **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="51896-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="51896-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="51896-111">**lpRes**</span></span>
  
> <span data-ttu-id="51896-112">Указатель на структуру [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="51896-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="51896-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="51896-113">**lpProp**</span></span>
  
> <span data-ttu-id="51896-114">Указатель на массив структур [SPropValue](spropvalue.md) , каждый из которых содержит тег свойства и значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="51896-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="51896-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="51896-115">Remarks</span></span>

<span data-ttu-id="51896-116">Структура **SCommentRestriction** связывает объект вместе с набор именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="51896-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="51896-117">Ограничения комментарий, в отличие от других ограничений, так как они не будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="51896-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="51896-118">То есть они обрабатываются с помощью метода [IMAPITable::Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="51896-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="51896-119">Она не влияет на строк, возвращаемых методом [IMAPITable::QueryRows](imapitable-queryrows.md) после вызова **IMAPITable::Restrict** .</span><span class="sxs-lookup"><span data-stu-id="51896-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="51896-120">Структура **SCommentRestriction** можно использовать для хранения сведений о приложении с ограничением при сохранении на диске.</span><span class="sxs-lookup"><span data-stu-id="51896-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="51896-121">Например клиент, сохранение имя именованного свойства, используемые в ограничении свойства можно сделать в структуре **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="51896-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="51896-122">Сохранение имя свойства не возможно в ограничение свойства, так как связанного структура [SPropertyRestriction](spropertyrestriction.md) содержит только тега свойства.</span><span class="sxs-lookup"><span data-stu-id="51896-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="51896-123">Дополнительные сведения о структуре **SCommentRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="51896-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51896-124">См. также</span><span class="sxs-lookup"><span data-stu-id="51896-124">See also</span></span>



[<span data-ttu-id="51896-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="51896-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="51896-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="51896-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="51896-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="51896-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="51896-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="51896-128">MAPI Structures</span></span>](mapi-structures.md)

