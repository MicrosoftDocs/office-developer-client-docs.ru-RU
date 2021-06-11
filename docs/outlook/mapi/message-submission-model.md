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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421125"
---
# <a name="message-submission-model"></a><span data-ttu-id="410db-103">Модель отправки сообщений</span><span class="sxs-lookup"><span data-stu-id="410db-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="410db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="410db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="410db-105">Отправка сообщений выполняется серией вызовов из пульпера MAPI поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="410db-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="410db-106">Вызовы последовательно следуют следующим образом:</span><span class="sxs-lookup"><span data-stu-id="410db-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="410db-107">Spooler MAPI вызывает [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), передав экземпляр [IMESSage : IMAPIProp,](imessageimapiprop.md) чтобы начать процесс.</span><span class="sxs-lookup"><span data-stu-id="410db-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="410db-108">Затем поставщик транспорта помещает эталонное значение — идентификатор, определенный транспортом, используемый в будущих ссылках на это сообщение , в расположении, на котором ссылается **в SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="410db-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="410db-109">Поставщик транспорта имеет доступ к данным сообщений с помощью переданного **экземпляра IMessage.**</span><span class="sxs-lookup"><span data-stu-id="410db-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="410db-110">Для каждого получателя в переданной **службе IMessage,** за которую он принимает ответственность, поставщик транспорта задает **свойство** [PR_RESPONSIBILITY (PidTagResponsibility),](pidtagresponsibility-canonical-property.md)а затем возвращается.</span><span class="sxs-lookup"><span data-stu-id="410db-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="410db-111">Поставщик транспорта может использовать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать, распознает ли он получателей, которые не могут быть доставлены, или создать стандартный отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="410db-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="410db-112">**StatusRecips** — это удобство для транспортных поставщиков, которые определили, что некоторые из получателей не могут быть доставлены или получили данные о доставке из их системы обмена сообщениями, которые могут оказаться полезными для пользователя или клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="410db-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="410db-113">Вызов шпалеров MAPI в [IXPLogon::EndMessage](ixplogon-endmessage.md) — это последняя отдача ответственности за сообщение от пулера MAPI поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="410db-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="410db-114">Шпалер MAPI может использовать [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для отмены обработки сообщений во время вызовов **SubmitMessage** или **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="410db-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

