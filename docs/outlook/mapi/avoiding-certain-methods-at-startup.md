---
title: Запуск без использования определенных методов
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808118"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="f4255-103">Запуск без использования определенных методов</span><span class="sxs-lookup"><span data-stu-id="f4255-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="f4255-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4255-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4255-105">В целях повышения производительности во время запуска предотвратить выполнение следующих вызовов:</span><span class="sxs-lookup"><span data-stu-id="f4255-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="f4255-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="f4255-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="f4255-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="f4255-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="f4255-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="f4255-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="f4255-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="f4255-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="f4255-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f4255-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="f4255-111">Вызов **IMAPIStatus::ValidateState** влияет на производительность только в том случае, когда для очереди MAPI или в подсистеме MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4255-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="f4255-112">Причина медленно, что эти методы запуска обработки том, что не удается выполнить до завершения задачи по запуску диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4255-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="f4255-113">Также следует избегать поиска хранилища сообщений во время запуска.</span><span class="sxs-lookup"><span data-stu-id="f4255-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="f4255-114">Выполнение звонков [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) после завершения работы запуска обработки.</span><span class="sxs-lookup"><span data-stu-id="f4255-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

