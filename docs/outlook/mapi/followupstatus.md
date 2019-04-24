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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327526"
---
# <a name="followupstatus"></a><span data-ttu-id="bacca-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="bacca-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="bacca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bacca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bacca-105">Задает различные статусы дальнейших действий для сообщения.</span><span class="sxs-lookup"><span data-stu-id="bacca-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bacca-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bacca-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="bacca-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bacca-107">Members</span></span>

 <span data-ttu-id="bacca-108">_Флвупноне_</span><span class="sxs-lookup"><span data-stu-id="bacca-108">_flwupNone_</span></span>
  
> <span data-ttu-id="bacca-109">Дальнейшие действия не указаны.</span><span class="sxs-lookup"><span data-stu-id="bacca-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="bacca-110">_Флвупкомплете_</span><span class="sxs-lookup"><span data-stu-id="bacca-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="bacca-111">Сообщение завершено.</span><span class="sxs-lookup"><span data-stu-id="bacca-111">The message is complete.</span></span>
    
 <span data-ttu-id="bacca-112">_Флвупмаркед_</span><span class="sxs-lookup"><span data-stu-id="bacca-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="bacca-113">Сообщение помечено для дальнейших действий.</span><span class="sxs-lookup"><span data-stu-id="bacca-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="bacca-114">_Флвупмакс_</span><span class="sxs-lookup"><span data-stu-id="bacca-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="bacca-115">Количество различных состояний, поддерживаемых для дальнейших действий.</span><span class="sxs-lookup"><span data-stu-id="bacca-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bacca-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bacca-116">See also</span></span>



[<span data-ttu-id="bacca-117">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="bacca-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

