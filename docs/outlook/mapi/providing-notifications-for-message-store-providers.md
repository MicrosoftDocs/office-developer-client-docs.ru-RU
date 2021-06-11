---
title: Предоставление уведомлений для поставщиков магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419935"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="0bc4f-103">Предоставление уведомлений для поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="0bc4f-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="0bc4f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bc4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bc4f-105">Хотя уведомления являются необязательными, они являются очень важной частью хорошего поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="0bc4f-106">Клиентские приложения и шпалер MAPI полагаются на уведомления от поставщика магазина сообщений, чтобы получить хорошую производительность при отправке исходящие сообщения или получении входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="0bc4f-107">Клиенты и шпалер MAPI могут работать без получения уведомлений от поставщика магазина сообщений, но без них они не смогут информировать пользователей об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="0bc4f-108">Как правило, это означает, что пользователи не смогут увидеть, что новое сообщение прибыло, пока их клиент не откроет папку получения в магазине сообщений.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="0bc4f-109">Клиенты регистрируются для получения уведомлений, вызывая [метод IMsgStore::Advise.](imsgstore-advise.md)</span><span class="sxs-lookup"><span data-stu-id="0bc4f-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="0bc4f-110">Клиент проходит в [интерфейсе IMAPIAdviseSink : IUnknown,](imapiadvisesinkiunknown.md) битмаске, которая указывает, какой тип уведомлений клиент заинтересован в получении, и  **entryID,** который указывает, к какому объекту в хранилище сообщений применяется запрос "Совет".</span><span class="sxs-lookup"><span data-stu-id="0bc4f-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="0bc4f-111">Если в объекте происходят соответствующие события (например, когда новое сообщение поступает в папку получения в хранилище сообщений), поставщику магазина сообщений или самому объекту следует вызвать [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для всех объектов **IMAPIAdviseSink,** зарегистрированных для этого типа событий.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="0bc4f-112">Даже если поставщик хранения сообщений никогда не сообщает другим компонентам MAPI об изменениях в хранилище сообщений, он по-прежнему должен реализовать **IMsgStore:::Advise** для возврата MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="0bc4f-113">Это информирует другие компоненты, чтобы не ожидать уведомлений от поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="0bc4f-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bc4f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc4f-114">See also</span></span>



[<span data-ttu-id="0bc4f-115">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="0bc4f-115">Message Store Features</span></span>](message-store-features.md)

