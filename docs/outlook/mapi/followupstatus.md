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
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568520"
---
# <a name="followupstatus"></a><span data-ttu-id="fcdb7-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="fcdb7-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="fcdb7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcdb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcdb7-105">Указывает различные состояния обработки результатов для сообщения.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fcdb7-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fcdb7-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="fcdb7-107">Members</span><span class="sxs-lookup"><span data-stu-id="fcdb7-107">Members</span></span>

 <span data-ttu-id="fcdb7-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="fcdb7-108">_flwupNone_</span></span>
  
> <span data-ttu-id="fcdb7-109">Нет исполнения не указана.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="fcdb7-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="fcdb7-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="fcdb7-111">Сообщение будет завершена.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-111">The message is complete.</span></span>
    
 <span data-ttu-id="fcdb7-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="fcdb7-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="fcdb7-113">Сообщение помечено для исполнения.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="fcdb7-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="fcdb7-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="fcdb7-115">Количество различных статусов, поддерживаемые для исполнения.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcdb7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fcdb7-116">See also</span></span>



[<span data-ttu-id="fcdb7-117">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="fcdb7-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

