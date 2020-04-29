---
title: Предоставление уведомлений для поставщиков хранилищ сообщений
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
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="62d84-103">Предоставление уведомлений для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="62d84-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="62d84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62d84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62d84-105">В то время как уведомления являются необязательными, это очень важная часть хорошего поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="62d84-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="62d84-106">Клиентские приложения и Диспетчер очереди MAPI используют Уведомления от поставщика хранилища сообщений для достижения оптимальной производительности при отправке исходящих сообщений или получении входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="62d84-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="62d84-107">Клиенты и Диспетчер очереди MAPI могут работать без уведомлений от поставщика хранилища сообщений, но они не смогут уведомлять пользователей об изменениях в хранилище сообщений без необходимости.</span><span class="sxs-lookup"><span data-stu-id="62d84-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="62d84-108">Как правило, это означает, что пользователи не смогут увидеть, что новое сообщение было доставлено до того момента, когда его клиент откроет папку получения хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="62d84-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="62d84-109">Клиенты регистрируются для получения уведомлений, вызывая метод [IMsgStore:: Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="62d84-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="62d84-110">Клиент передает [имапиадвисесинк: интерфейс IUnknown](imapiadvisesinkiunknown.md) , битовую маску, указывающую тип уведомлений, которые получает клиент, и идентификатор **EntryID** , указывающий на объект в хранилище сообщений, к которому применяется запрос **advise** .</span><span class="sxs-lookup"><span data-stu-id="62d84-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="62d84-111">При возникновении в объекте релевантных событий (например, когда новое сообщение поступает в папку Receive в хранилище сообщений), поставщик хранилища сообщений или сам объект должен вызвать метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для всех объектов **имапиадвисесинк** , зарегистрированных для этого типа события.</span><span class="sxs-lookup"><span data-stu-id="62d84-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="62d84-112">Даже если поставщик хранилища сообщений никогда не уведомляет другие компоненты MAPI об изменениях в хранилище сообщений, он по-прежнему должен реализовывать **IMsgStore:: Advise** для возврата MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="62d84-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="62d84-113">Это информирует другие компоненты о том, что не ожидаются уведомления от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="62d84-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62d84-114">См. также</span><span class="sxs-lookup"><span data-stu-id="62d84-114">See also</span></span>



[<span data-ttu-id="62d84-115">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="62d84-115">Message Store Features</span></span>](message-store-features.md)

