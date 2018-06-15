---
title: Модель приема сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19810011"
---
# <a name="message-reception-model"></a><span data-ttu-id="e6178-103">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="e6178-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="e6178-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6178-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6178-105">Поставщик транспорта управляет ли диспетчер очереди MAPI должен опроса его для входящей почты или ли оно выполняет вызов диспетчер очереди MAPI при поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6178-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="e6178-106">Поставщика транспорта устанавливает флаг SP_LOGON_POLL при возврате из [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для запроса опроса.</span><span class="sxs-lookup"><span data-stu-id="e6178-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="e6178-107">В противном случае поставщика транспорта использует [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) при входящей почты.</span><span class="sxs-lookup"><span data-stu-id="e6178-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="e6178-108">После обучения, что входящую почту, доступен, диспетчер очереди MAPI откроется новое сообщение и запрашивает поставщика транспорта для хранения свойства полученного сообщения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="e6178-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="e6178-109">Этот процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e6178-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="e6178-110">Доступные сообщения указываются с любого из поставщика транспорта, вызов **IMAPISupport::SpoolerNotify** или диспетчер очереди MAPI, вызов [IXPLogon::Poll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="e6178-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="e6178-111">Диспетчер очереди MAPI вызывает [IXPLogon::StartMessage](ixplogon-startmessage.md) для запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="e6178-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="e6178-112">Поставщика транспорта устанавливает значение ссылки в расположение, на который ссылается **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="e6178-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="e6178-113">Эти значения ссылку разрешить поставщика транспорта и диспетчер очереди MAPI для отслеживания сообщений, обрабатывается при наличии нескольких сообщения для доставки.</span><span class="sxs-lookup"><span data-stu-id="e6178-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="e6178-114">Поставщика транспорта хранит данные сообщений в передаваемый [IMessage: IMAPIProp](imessageimapiprop.md) экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e6178-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="e6178-115">Поставщика транспорта вызывается метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) **IMessage** экземпляра и возвращает из **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="e6178-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="e6178-116">Диспетчер очереди MAPI вызывает [IXPLogon::TransportNotify](ixplogon-transportnotify.md) , если ее необходимо остановить доставки сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6178-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e6178-117">Если поставщика транспорта используется **IMAPISupport::SpoolerNotify** вместо **IXPLogon::Poll**поставщика транспорта должна предоставить большое число сообщений, следует соблюдать осторожность не для вызова **SpoolerNotify** слишком часто в порядке, чтобы не привести другими поставщиками транспорта времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="e6178-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="e6178-118">Диспетчер очереди MAPI имеют логику, чтобы предотвратить это, но в целом интервал между вызовами **SpoolerNotify** должно быть длиннее время, затраченное поставщика транспорта для обработки одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6178-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="e6178-119">> Кроме того диспетчер очереди MAPI может обрабатывать входящие сообщения сразу же.</span><span class="sxs-lookup"><span data-stu-id="e6178-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="e6178-120">Диспетчер очереди MAPI может потребоваться поставщика транспорта для выполнения других задач до получения входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6178-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

