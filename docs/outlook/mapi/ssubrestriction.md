---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581960"
---
# <a name="ssubrestriction"></a><span data-ttu-id="07cb7-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="07cb7-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="07cb7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07cb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07cb7-105">Описываются ограничения дочерний объект, который используется для фильтрации строк вложения сообщения или получателей в таблице.</span><span class="sxs-lookup"><span data-stu-id="07cb7-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07cb7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="07cb7-106">Header file:</span></span>  <br/> |<span data-ttu-id="07cb7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07cb7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="07cb7-108">Members</span><span class="sxs-lookup"><span data-stu-id="07cb7-108">Members</span></span>

 <span data-ttu-id="07cb7-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="07cb7-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="07cb7-110">Тип дочерний объект в качестве целевого для ограничения.</span><span class="sxs-lookup"><span data-stu-id="07cb7-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="07cb7-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cb7-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="07cb7-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="07cb7-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="07cb7-113">Ограничения применяются к таблице получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="07cb7-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="07cb7-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="07cb7-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="07cb7-115">Ограничения применяются к таблице вложений сообщений.</span><span class="sxs-lookup"><span data-stu-id="07cb7-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="07cb7-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="07cb7-116">**lpRes**</span></span>
  
> <span data-ttu-id="07cb7-117">Указатель на структуру [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="07cb7-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="07cb7-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="07cb7-118">Remarks</span></span>

<span data-ttu-id="07cb7-119">Ограничения дочерних объектов не поддерживаются все таблицы.</span><span class="sxs-lookup"><span data-stu-id="07cb7-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="07cb7-120">Как правило содержимого только папки таблиц и их поддержка папок результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="07cb7-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="07cb7-121">Например ограничения дочерний объект используются для найдите сообщение, которое имеет определенный тип вложения или получателя.</span><span class="sxs-lookup"><span data-stu-id="07cb7-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="07cb7-122">Если реализация не поддерживает ограничения дочерний объект, она возвращает MAPI_E_TOO_COMPLEX методов [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="07cb7-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="07cb7-123">Общие сведения о работе ограничения обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="07cb7-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07cb7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="07cb7-124">See also</span></span>



[<span data-ttu-id="07cb7-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="07cb7-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="07cb7-126">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="07cb7-126">MAPI Structures</span></span>](mapi-structures.md)

