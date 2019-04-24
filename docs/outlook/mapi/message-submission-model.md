---
title: Модель отправки сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356877"
---
# <a name="message-submission-model"></a><span data-ttu-id="2d061-103">Модель отправки сообщений</span><span class="sxs-lookup"><span data-stu-id="2d061-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="2d061-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d061-105">Отправка сообщений выполняется с помощью ряда вызовов от диспетчера очереди MAPI к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="2d061-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="2d061-106">Звонки упорядочены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d061-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="2d061-107">Диспетчер очереди MAPI вызывает [иксплогон:: субмитмессаже](ixplogon-submitmessage.md), передавая экземпляр [iMessage: IMAPIProp](imessageimapiprop.md) , чтобы приступить к процессу.</span><span class="sxs-lookup"><span data-stu-id="2d061-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="2d061-108">Затем поставщик транспорта помещает значение ссылки (идентификатор, определенный транспортом), используемый в дальнейших ссылках на это сообщение, в расположении, указанном в **субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="2d061-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="2d061-109">Поставщик транспорта получает доступ к данным сообщения с помощью передаваемого экземпляра **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="2d061-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="2d061-110">Для каждого получателя в переданном **iMessage** , для которого он принимает ответственность, поставщик транспорта задает свойство **пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), а затем возвращает.</span><span class="sxs-lookup"><span data-stu-id="2d061-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="2d061-111">Поставщик транспорта может использовать метод [имаписуппорт:: статусреЦипс](imapisupport-statusrecips.md) , чтобы определить, распознают ли они тех получателей, которые не могут быть доставлены, или создать стандартный отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="2d061-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="2d061-112">**СтатусреЦипс** — это удобство для поставщиков транспорта, которые определили, что некоторые из получателей не могут быть доставлены или получали сведения о доставке от своей базовой системы обмена сообщениями, которую может выполнять пользователь или клиентское приложение. получите полезную возможность.</span><span class="sxs-lookup"><span data-stu-id="2d061-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="2d061-113">Вызов [иксплогон:: ендмессаже](ixplogon-endmessage.md) — это последняя ответственность за отправку сообщений от очереди MAPI к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="2d061-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="2d061-114">Диспетчер очереди MAPI может использовать [иксплогон:: транспортнотифи](ixplogon-transportnotify.md) для отмены обработки сообщений во время вызовов **субмитмессаже** или **ендмессаже** .</span><span class="sxs-lookup"><span data-stu-id="2d061-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

