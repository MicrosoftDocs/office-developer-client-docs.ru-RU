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
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808461"
---
# <a name="followupstatus"></a><span data-ttu-id="aac65-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="aac65-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="aac65-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aac65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aac65-105">Указывает различные состояния обработки результатов для сообщения.</span><span class="sxs-lookup"><span data-stu-id="aac65-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aac65-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="aac65-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="aac65-107">Members</span><span class="sxs-lookup"><span data-stu-id="aac65-107">Members</span></span>

 <span data-ttu-id="aac65-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="aac65-108">_flwupNone_</span></span>
  
> <span data-ttu-id="aac65-109">Нет исполнения не указана.</span><span class="sxs-lookup"><span data-stu-id="aac65-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="aac65-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="aac65-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="aac65-111">Сообщение будет завершена.</span><span class="sxs-lookup"><span data-stu-id="aac65-111">The message is complete.</span></span>
    
 <span data-ttu-id="aac65-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="aac65-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="aac65-113">Сообщение помечено для исполнения.</span><span class="sxs-lookup"><span data-stu-id="aac65-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="aac65-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="aac65-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="aac65-115">Количество различных статусов, поддерживаемые для исполнения.</span><span class="sxs-lookup"><span data-stu-id="aac65-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aac65-116">См. также</span><span class="sxs-lookup"><span data-stu-id="aac65-116">See also</span></span>



[<span data-ttu-id="aac65-117">Каноническое свойство PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="aac65-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

