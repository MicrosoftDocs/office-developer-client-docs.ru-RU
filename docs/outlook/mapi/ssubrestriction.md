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
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406327"
---
# <a name="ssubrestriction"></a><span data-ttu-id="199c1-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="199c1-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="199c1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="199c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="199c1-105">Описывает ограничение вложенного объекта, которое используется для фильтрации строк в таблице вложения или получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="199c1-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="199c1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="199c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="199c1-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="199c1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="199c1-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="199c1-108">Members</span></span>

 <span data-ttu-id="199c1-109">**улсубобжект**</span><span class="sxs-lookup"><span data-stu-id="199c1-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="199c1-110">Тип дочернего объекта, который будет использоваться в качестве целевого для ограничения.</span><span class="sxs-lookup"><span data-stu-id="199c1-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="199c1-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="199c1-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="199c1-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="199c1-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="199c1-113">Применить ограничение к таблице получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="199c1-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="199c1-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="199c1-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="199c1-115">Примените ограничение к таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="199c1-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="199c1-116">**лпрес**</span><span class="sxs-lookup"><span data-stu-id="199c1-116">**lpRes**</span></span>
  
> <span data-ttu-id="199c1-117">Указатель на структуру [срестриктион](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="199c1-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="199c1-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="199c1-118">Remarks</span></span>

<span data-ttu-id="199c1-119">Ограничения на вложенные объекты не поддерживаются всеми таблицами.</span><span class="sxs-lookup"><span data-stu-id="199c1-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="199c1-120">Как правило, эти таблицы поддерживают только таблицы содержимого папок и папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="199c1-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="199c1-121">Например, ограничения на вложенные объекты используются для поиска сообщения с определенным типом вложения или получателя.</span><span class="sxs-lookup"><span data-stu-id="199c1-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="199c1-122">Если реализация не поддерживает ограничения на вложенные объекты, она возвращает MAPI_E_TOO_COMPLEX от методов [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="199c1-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="199c1-123">Общие сведения о том, как действуют ограничения, можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="199c1-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="199c1-124">См. также</span><span class="sxs-lookup"><span data-stu-id="199c1-124">See also</span></span>



[<span data-ttu-id="199c1-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="199c1-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="199c1-126">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="199c1-126">MAPI Structures</span></span>](mapi-structures.md)

