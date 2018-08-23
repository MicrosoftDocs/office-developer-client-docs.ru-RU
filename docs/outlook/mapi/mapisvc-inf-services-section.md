---
title: 'MapiSvc.inf: раздел [Службы]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571397"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="e2fda-103">MapiSvc.inf: раздел [Службы]</span><span class="sxs-lookup"><span data-stu-id="e2fda-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="e2fda-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2fda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2fda-105">В разделе **[Services]** перечислены службы сообщений, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e2fda-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="e2fda-106">Записи в этом разделе используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="e2fda-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="e2fda-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="e2fda-107">**[Services]**</span></span>
  
 <span data-ttu-id="e2fda-108">_Имя раздела службы сообщений_ =  _имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="e2fda-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="e2fda-109">Имя раздела службы сообщений — это строка, определенного службой сообщения для ссылки в этой записи в соответствующий раздел для службы в любом месте mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="e2fda-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="e2fda-110">Имя службы сообщений — это имя службы, установленные.</span><span class="sxs-lookup"><span data-stu-id="e2fda-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="e2fda-111">В следующем разделе описываются три службы сообщений: адресной книги по умолчанию, мои собственные службы и службы хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e2fda-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="e2fda-112">Эти службы, вымышленной только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="e2fda-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="e2fda-113">Разработчик службы каждого сообщения подставить средством для свой службы сообщений в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e2fda-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="e2fda-114">Каждая запись в данном разделе имеет соответствующий раздел собственных хранения сведений о службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="e2fda-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="e2fda-115">Например соответствующий раздел для адресной книги по умолчанию называется [AB].</span><span class="sxs-lookup"><span data-stu-id="e2fda-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

