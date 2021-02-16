---
title: Обработка поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416540"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="6e330-103">Обработка поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="6e330-103">Handling a transport provider</span></span>
  
<span data-ttu-id="6e330-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e330-105">Клиенты взаимодействуют с поставщиками транспорта через объекты состояния, предоставленные поставщиками транспорта и пулом MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e330-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="6e330-106">Клиенты получают доступ к объектам состояния, вызывая [IMAPISession::GetStatusTable для](imapisession-getstatustable.md) получения таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="6e330-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="6e330-107">Объекты состояния реализуют интерфейс [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) который имеет методы для настройки поставщиков, очистки очередей входящих и исходяющих сообщений, установки паролей и проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="6e330-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="6e330-108">Дополнительные сведения об объектах состояния см. в [таблицах status Table и Status Objects.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="6e330-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="6e330-109">[Отправка или получение сообщения по запросу](sending-or-receiving-a-message-on-demand.md): описывает отправку или получение сообщения по требованию.</span><span class="sxs-lookup"><span data-stu-id="6e330-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="6e330-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span><span class="sxs-lookup"><span data-stu-id="6e330-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="6e330-111">[Перенастройка поставщика](reconfiguring-a-transport-provider.md)транспорта: описывается, как перенастроить поставщика транспорта и какие свойства можно настроить.</span><span class="sxs-lookup"><span data-stu-id="6e330-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

