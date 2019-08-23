---
title: Уклонение от использования определенных методов при запуске
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Дата последнего изменения: 7 декабря 2015 года'
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318090"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="1f46c-103">Уклонение от использования определенных методов при запуске</span><span class="sxs-lookup"><span data-stu-id="1f46c-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="1f46c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f46c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f46c-105">Для повышения производительности в момент запуска, не используйте указанные ниже вызовы:</span><span class="sxs-lookup"><span data-stu-id="1f46c-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="1f46c-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="1f46c-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="1f46c-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="1f46c-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="1f46c-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="1f46c-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="1f46c-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="1f46c-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="1f46c-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="1f46c-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="1f46c-111">Вызов **IMAPIStatus::ValidateState** влияет на производительность только в случае использования либо программы буферизации данных MAPI, подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f46c-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="1f46c-112">Причина, по которой эти методы замедляют процесс запуска, заключается в том, что их нельзя выполнить, пока программа буферизации данных MAPI не завершит все задачи при запуске.</span><span class="sxs-lookup"><span data-stu-id="1f46c-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="1f46c-113">Кроме того, следует избегать поиска хранилища сообщений в момент запуска.</span><span class="sxs-lookup"><span data-stu-id="1f46c-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="1f46c-114">Выполните вызов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) после завершения обработки запуска.</span><span class="sxs-lookup"><span data-stu-id="1f46c-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

