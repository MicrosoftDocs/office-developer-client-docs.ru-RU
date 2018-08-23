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
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567953"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="8f91c-103">Обработка поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="8f91c-103">Handling a transport provider</span></span>
  
<span data-ttu-id="8f91c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f91c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f91c-105">Клиенты связываться с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="8f91c-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="8f91c-106">Клиенты доступа к объектам состояние путем вызова [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="8f91c-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="8f91c-107">Объекты состояния реализовать [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейс, который содержит методы для настройки поставщиков, очистки входящих и исходящих сообщений очереди, установка паролей и проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="8f91c-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="8f91c-108">Дополнительные сведения о состоянии объекты можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8f91c-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="8f91c-109">[Отправки и получения сообщений по требованию](sending-or-receiving-a-message-on-demand.md): описывается, как отправлять и получать сообщения по запросу.</span><span class="sxs-lookup"><span data-stu-id="8f91c-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="8f91c-110">[Параметр транспорта заказа](setting-transport-order.md): описывается, как установить порядок транспорта.</span><span class="sxs-lookup"><span data-stu-id="8f91c-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="8f91c-111">[Перенастройка поставщика транспорта](reconfiguring-a-transport-provider.md): описание повторно настройте поставщика транспорта и какие свойства доступны для установки.</span><span class="sxs-lookup"><span data-stu-id="8f91c-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

