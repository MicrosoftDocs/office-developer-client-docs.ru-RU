---
title: MapiSvc.inf [Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434783"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="0e6c8-103">MapiSvc.inf [Services] Section</span><span class="sxs-lookup"><span data-stu-id="0e6c8-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="0e6c8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e6c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e6c8-105">В **разделе [Службы]** перечислены службы сообщений, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="0e6c8-106">Записи в этом разделе используют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0e6c8-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="0e6c8-107">**[Службы]**</span><span class="sxs-lookup"><span data-stu-id="0e6c8-107">**[Services]**</span></span>
  
 <span data-ttu-id="0e6c8-108">_имя раздела службы сообщений_  =   _имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="0e6c8-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="0e6c8-109">Имя раздела службы сообщений — это строка, определяемая службой сообщений, которая связывает эту запись с соответствующим разделом для службы в другом месте mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="0e6c8-110">Имя службы сообщений — это имя установленной службы.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="0e6c8-111">В следующем разделе показаны три службы сообщений: адресная книга по умолчанию, моя собственная служба и служба магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="0e6c8-112">Эти службы являются вымышленными только в целях иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="0e6c8-113">Каждый реализующий службу сообщений заменит соответствующую запись для своей службы сообщений в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="0e6c8-114">Каждая запись в этом разделе имеет собственный раздел, в котором хранятся сведения для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0e6c8-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="0e6c8-115">Например, соответствующий раздел адресной книги по умолчанию называется [AB].</span><span class="sxs-lookup"><span data-stu-id="0e6c8-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

