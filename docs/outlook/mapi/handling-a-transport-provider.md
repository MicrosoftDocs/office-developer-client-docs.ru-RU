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
ms.openlocfilehash: 140fe97662f7a2ce68c18d8e0eb991d0819da6dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808540"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="9b1d4-103">Обработка поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="9b1d4-103">Handling a transport provider</span></span>
  
<span data-ttu-id="9b1d4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b1d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b1d4-105">Клиенты связываться с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="9b1d4-106">Клиенты доступа к объектам состояние путем вызова [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="9b1d4-107">Объекты состояния реализовать [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейс, который содержит методы для настройки поставщиков, очистки входящих и исходящих сообщений очереди, установка паролей и проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="9b1d4-108">Дополнительные сведения о состоянии объекты можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9b1d4-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="9b1d4-109">[Отправки и получения сообщений по требованию](sending-or-receiving-a-message-on-demand.md): описывается, как отправлять и получать сообщения по запросу.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="9b1d4-110">[Параметр транспорта заказа](setting-transport-order.md): описывается, как установить порядок транспорта.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="9b1d4-111">[Перенастройка поставщика транспорта](reconfiguring-a-transport-provider.md): описание повторно настройте поставщика транспорта и какие свойства доступны для установки.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

