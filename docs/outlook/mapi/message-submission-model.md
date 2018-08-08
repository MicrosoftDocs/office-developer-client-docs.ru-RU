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
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810031"
---
# <a name="message-submission-model"></a><span data-ttu-id="d2ac8-103">Модель отправки сообщений</span><span class="sxs-lookup"><span data-stu-id="d2ac8-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="d2ac8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2ac8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2ac8-105">Передача сообщений выполняется путем последовательности вызовов из очереди MAPI для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="d2ac8-106">Вызовы упорядочены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2ac8-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="d2ac8-107">Диспетчер очереди MAPI вызывает [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), передав в [IMessage: IMAPIProp](imessageimapiprop.md) экземпляр, чтобы начать процесс.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="d2ac8-108">Поставщика транспорта затем помещает значение ссылки — определенный идентификатор транспорта используется в следующих ссылок на это сообщение, в расположении, на который ссылается **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="d2ac8-109">Поставщика транспорта получает доступ к данным сообщений с помощью переданный экземпляры **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="d2ac8-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="d2ac8-110">Для каждого получателя в переданных **IMessage** , для которого он принимает ответственность за поставщика транспорта устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) и затем возвращает.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="d2ac8-111">Чтобы указать, если он распознает получателей, которые невозможно доставить или для создания отчетов о доставке standard, поставщика транспорта можно использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ac8-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="d2ac8-112">**StatusRecips** является удобство для поставщиков транспорта, которые определено, что некоторые из получателей невозможно доставить или от их базовой системы обмена сообщениями, который может пользователя или клиентских приложений, который был получен сведений о доставке оказаться полезными.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="d2ac8-113">Диспетчер очереди MAPI вызов [IXPLogon::EndMessage](ixplogon-endmessage.md) отключен окончательный ответственности наличии-сообщения из очереди MAPI для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="d2ac8-114">Диспетчер очереди MAPI можно использовать [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для отмены обработки при выполнении вызова **SubmitMessage** или **EndMessage** сообщения.</span><span class="sxs-lookup"><span data-stu-id="d2ac8-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

