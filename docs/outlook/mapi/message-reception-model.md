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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415119"
---
# <a name="message-reception-model"></a><span data-ttu-id="0cb3d-103">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="0cb3d-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="0cb3d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cb3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cb3d-105">Поставщик транспорта контролирует, должен ли шпалер MAPI опросить ее для входящих сообщений или выполняет ли он вызов обратно в пульпер MAPI по прибытии новой почты.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="0cb3d-106">Поставщик транспорта задает флаг SP_LOGON_POLL, когда он возвращается из [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для запроса опроса.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="0cb3d-107">В противном случае поставщик транспорта использует [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) при наличии входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="0cb3d-108">Узнав о наличии входящих сообщений, пуллер MAPI открывает новое сообщение и просит поставщика транспорта хранить полученные свойства сообщения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="0cb3d-109">Этот процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0cb3d-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="0cb3d-110">Доступные сообщения указываются либо поставщиком транспорта по вызову **IMAPISupport::SpoolerNotify,** либо пулером MAPI, который вызывает [IXPLogon::P oll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3d-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="0cb3d-111">Шпалер MAPI вызывает [IXPLogon::StartMessage](ixplogon-startmessage.md) для инициации процесса.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="0cb3d-112">Поставщик транспорта помещает справочные значения в расположении, на который ссылается **StartMessage.**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="0cb3d-113">Эти справочные значения позволяют поставщику транспорта и шпалеру MAPI отслеживать, какое сообщение обрабатывается при доставке нескольких сообщений.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="0cb3d-114">Поставщик транспорта хранит данные сообщений в переданный [экземпляр IMessage : IMAPIProp.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="0cb3d-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="0cb3d-115">Поставщик транспорта вызывает [метод IMAPIProp::SaveChanges](imapiprop-savechanges.md) в **экземпляре IMessage** и возвращается из **StartMessage.**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="0cb3d-116">Spooler MAPI вызывает [IXPLogon::TransportNotify,](ixplogon-transportnotify.md) если необходимо остановить доставку сообщений.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="0cb3d-117">Если поставщик транспорта должен доставить большое количество сообщений, а поставщик транспорта использует **IMAPISupport::SpoolerNotify** вместо **IXPLogon::P oll,** необходимо не вызывать **SpoolerNotify** слишком часто, чтобы не лишать других поставщиков транспорта времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="0cb3d-118">У шпалеров MAPI есть логика, чтобы предотвратить это, но в целом интервал между вызовами **SpoolerNotify** должен быть больше времени, которое требуется поставщику транспорта для обработки одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="0cb3d-119">> кроме того, шпалер MAPI может не обрабатывать входящие сообщения немедленно.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="0cb3d-120">Шпалер MAPI может попросить поставщика транспорта выполнить другие задачи перед получением входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

