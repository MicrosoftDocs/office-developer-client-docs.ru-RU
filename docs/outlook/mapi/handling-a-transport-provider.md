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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299498"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="bf499-103">Обработка поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="bf499-103">Handling a transport provider</span></span>
  
<span data-ttu-id="bf499-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf499-105">Клиенты взаимодействуют с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчером очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf499-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="bf499-106">Клиенты получают доступ к объектам состояния, вызывая [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для получения таблицы Status.</span><span class="sxs-lookup"><span data-stu-id="bf499-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="bf499-107">Объекты Status реализуют интерфейс [имапистатус: IMAPIProp](imapistatusimapiprop.md) , который содержит методы для настройки поставщиков, очистки входящих и исходящих очередей сообщений, установки паролей и проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="bf499-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="bf499-108">Для получения дополнительных сведений об объектах состояния просмотрите [объекты состояния таблица и состояние](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bf499-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="bf499-109">[Отправка или получение сообщения по запросу](sending-or-receiving-a-message-on-demand.md): сведения о том, как отправлять или получать сообщение по запросу.</span><span class="sxs-lookup"><span data-stu-id="bf499-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="bf499-110">[Установка заказа](setting-transport-order.md)на транспортировку: в этой статье описывается, как задать транспортный заказ.</span><span class="sxs-lookup"><span data-stu-id="bf499-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="bf499-111">Повторная [Настройка поставщика транспорта](reconfiguring-a-transport-provider.md): в этой статье описывается порядок изменения конфигурации поставщика транспорта и свойств, доступных для установки.</span><span class="sxs-lookup"><span data-stu-id="bf499-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

