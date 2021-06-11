---
title: Раздел MapiSvc.inf [Services]
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
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="2e51a-103">Раздел MapiSvc.inf [Services]</span><span class="sxs-lookup"><span data-stu-id="2e51a-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="2e51a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e51a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e51a-105">В **разделе [Services]** перечислены службы сообщений, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2e51a-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="2e51a-106">Записи в этом разделе используют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="2e51a-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="2e51a-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="2e51a-107">**[Services]**</span></span>
  
 <span data-ttu-id="2e51a-108">_Имя раздела "служба сообщений"_  =   _Имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="2e51a-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="2e51a-109">Имя раздела служба сообщений — это строка, определяемая службой сообщений, которая связывает эту запись с соответствующим разделом для службы в другом месте в mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="2e51a-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="2e51a-110">Имя службы сообщений — это имя установленной службы.</span><span class="sxs-lookup"><span data-stu-id="2e51a-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="2e51a-111">В следующем разделе показаны три службы сообщений: адресная книга по умолчанию, моя собственная служба и служба магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e51a-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="2e51a-112">Эти службы являются вымышленными только для иллюстраций.</span><span class="sxs-lookup"><span data-stu-id="2e51a-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="2e51a-113">Каждый реализующий службу сообщений заменит соответствующую запись для службы сообщений в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="2e51a-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="2e51a-114">Каждая запись в этом разделе имеет соответствующий раздел, в котором хранятся сведения для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e51a-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="2e51a-115">Например, соответствующий раздел адресной книги по умолчанию называется [AB].</span><span class="sxs-lookup"><span data-stu-id="2e51a-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

