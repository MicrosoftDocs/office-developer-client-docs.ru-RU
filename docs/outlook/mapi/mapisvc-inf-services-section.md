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
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809908"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="9c442-103">MapiSvc.inf: раздел [Службы]</span><span class="sxs-lookup"><span data-stu-id="9c442-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="9c442-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c442-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c442-105">В разделе **[Services]** перечислены службы сообщений, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9c442-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="9c442-106">Записи в этом разделе используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9c442-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="9c442-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="9c442-107">**[Services]**</span></span>
  
 <span data-ttu-id="9c442-108">_Имя раздела службы сообщений_ =  _имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="9c442-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="9c442-109">Имя раздела службы сообщений — это строка, определенного службой сообщения для ссылки в этой записи в соответствующий раздел для службы в любом месте mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9c442-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="9c442-110">Имя службы сообщений — это имя службы, установленные.</span><span class="sxs-lookup"><span data-stu-id="9c442-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="9c442-111">В следующем разделе описываются три службы сообщений: адресной книги по умолчанию, мои собственные службы и службы хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c442-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="9c442-112">Эти службы, вымышленной только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="9c442-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="9c442-113">Разработчик службы каждого сообщения подставить средством для свой службы сообщений в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9c442-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="9c442-114">Каждая запись в данном разделе имеет соответствующий раздел собственных хранения сведений о службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c442-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="9c442-115">Например соответствующий раздел для адресной книги по умолчанию называется [AB].</span><span class="sxs-lookup"><span data-stu-id="9c442-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

