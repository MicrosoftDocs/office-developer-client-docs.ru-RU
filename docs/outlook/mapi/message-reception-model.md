---
title: Модель приема сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356947"
---
# <a name="message-reception-model"></a><span data-ttu-id="3aa64-103">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="3aa64-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="3aa64-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3aa64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3aa64-105">Поставщик транспорта определяет, должен ли диспетчер очереди MAPI опрашивать его для входящей почты, а также выполняется ли обратное вызов к диспетчеру очереди MAPI при поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="3aa64-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="3aa64-106">Поставщик транспорта устанавливает флаг СП_ЛОГОН_ПОЛЛ, когда он возвращается из [иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) , чтобы запросить опрос.</span><span class="sxs-lookup"><span data-stu-id="3aa64-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="3aa64-107">В противном случае поставщик транспорта использует [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) , когда доступна входящая почта.</span><span class="sxs-lookup"><span data-stu-id="3aa64-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="3aa64-108">После изучения того, что входящая почта доступна, диспетчер очереди MAPI открывает новое сообщение и запрашивает у поставщика транспорта сохранение свойств полученного сообщения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="3aa64-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="3aa64-109">Этот процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3aa64-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="3aa64-110">Доступные сообщения обозначаются поставщиком транспорта, вызывающим **имаписуппорт:: спулернотифи** или с помощью ДИСПЕТЧЕРА очереди MAPI вызов [иксплогон::P олл](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="3aa64-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="3aa64-111">Диспетчер очереди MAPI вызывает метод [иксплогон:: стартмессаже](ixplogon-startmessage.md) для запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="3aa64-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="3aa64-112">Поставщик транспорта помещает значение ссылки в расположении, указанном в **стартмессаже**.</span><span class="sxs-lookup"><span data-stu-id="3aa64-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="3aa64-113">Эти справочные значения позволяют поставщику транспорта и диспетчеру очереди MAPI следить за тем, какие сообщения обрабатываются при наличии нескольких сообщений.</span><span class="sxs-lookup"><span data-stu-id="3aa64-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="3aa64-114">Поставщик транспорта сохраняет данные сообщения в переданный экземпляр [iMessage: IMAPIProp](imessageimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa64-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="3aa64-115">Поставщик транспорта вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для экземпляра **iMessage** и возвращает из **стартмессаже**.</span><span class="sxs-lookup"><span data-stu-id="3aa64-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="3aa64-116">Диспетчер очереди MAPI вызывает метод [иксплогон:: транспортнотифи](ixplogon-transportnotify.md) , если он должен остановить доставку сообщений.</span><span class="sxs-lookup"><span data-stu-id="3aa64-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3aa64-117">Если поставщик транспорта должен доставлять большое количество сообщений, а поставщик транспорта использует **имаписуппорт:: спулернотифи** , а не **иксплогон::P олл**, будьте внимательны и не вызывайте **спулернотифи** слишком часто, чтобы не было деприве другие поставщики транспорта для времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="3aa64-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="3aa64-118">Диспетчер очереди MAPI имеет логику, которая предотвращает возникновение такой ситуации, но в общем случае интервал между вызовами **спулернотифи** должен быть больше, чем время, затраченное поставщиком транспорта на обработку одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3aa64-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="3aa64-119">_Гт_ Кроме того, диспетчер очереди MAPI может не обработать входящее сообщение сразу.</span><span class="sxs-lookup"><span data-stu-id="3aa64-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="3aa64-120">Диспетчер очереди MAPI может попросить поставщика транспорта выполнить другие задачи, прежде чем получать входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="3aa64-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

