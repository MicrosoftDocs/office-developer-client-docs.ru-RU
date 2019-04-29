---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418332"
---
# <a name="followupstatus"></a><span data-ttu-id="3b5d4-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="3b5d4-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="3b5d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b5d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b5d4-105">Задает различные статусы дальнейших действий для сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b5d4-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3b5d4-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3b5d4-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="3b5d4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="3b5d4-107">Members</span></span>

 <span data-ttu-id="3b5d4-108">_Флвупноне_</span><span class="sxs-lookup"><span data-stu-id="3b5d4-108">_flwupNone_</span></span>
  
> <span data-ttu-id="3b5d4-109">Дальнейшие действия не указаны.</span><span class="sxs-lookup"><span data-stu-id="3b5d4-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="3b5d4-110">_Флвупкомплете_</span><span class="sxs-lookup"><span data-stu-id="3b5d4-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="3b5d4-111">Сообщение завершено.</span><span class="sxs-lookup"><span data-stu-id="3b5d4-111">The message is complete.</span></span>
    
 <span data-ttu-id="3b5d4-112">_Флвупмаркед_</span><span class="sxs-lookup"><span data-stu-id="3b5d4-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="3b5d4-113">Сообщение помечено для дальнейших действий.</span><span class="sxs-lookup"><span data-stu-id="3b5d4-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="3b5d4-114">_Флвупмакс_</span><span class="sxs-lookup"><span data-stu-id="3b5d4-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="3b5d4-115">Количество различных состояний, поддерживаемых для дальнейших действий.</span><span class="sxs-lookup"><span data-stu-id="3b5d4-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b5d4-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3b5d4-116">See also</span></span>



[<span data-ttu-id="3b5d4-117">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="3b5d4-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

