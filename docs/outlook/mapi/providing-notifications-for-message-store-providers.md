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
ms.openlocfilehash: 3722893ae57a108b338725e46c975e92c0f8ff72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587511"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="c76fb-103">Предоставление уведомлений для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="c76fb-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="c76fb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c76fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c76fb-105">Хотя уведомления необязательно, они являются важной частью поставщика хранилища хороший сообщения.</span><span class="sxs-lookup"><span data-stu-id="c76fb-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="c76fb-106">Клиентские приложения и диспетчер очереди MAPI используют уведомления от поставщика хранилища сообщений для достижения высокой производительности при отправке исходящих сообщений или получение входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c76fb-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="c76fb-107">Клиенты и диспетчер очереди MAPI может работать без получения уведомления из поставщика хранилища сообщений, но они не смогут уведомить пользователей об изменениях в хранилище сообщений без их.</span><span class="sxs-lookup"><span data-stu-id="c76fb-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="c76fb-108">Как правило это означает, что пользователи не смогут видеть, что новое сообщение пришло до их клиент затем открывает хранилище сообщений получают папки.</span><span class="sxs-lookup"><span data-stu-id="c76fb-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="c76fb-109">Клиенты регистрируются для уведомлений путем вызова метода [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="c76fb-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="c76fb-110">Клиент передает в [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) интерфейса Битовая маска, которое указывает, какой тип уведомления клиента получать, и **идентификатор записи** , которое указывает, какой объект в сообщении хранения **уведомлений** применяет запроса.</span><span class="sxs-lookup"><span data-stu-id="c76fb-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="c76fb-111">При возникновении соответствующих событий в объект (например, при получении нового сообщения в папку получения в хранилище сообщений), поставщика хранилища сообщений или самого объекта должны вызывать метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для всех ** IMAPIAdviseSink** объекты, зарегистрированные для этого типа события.</span><span class="sxs-lookup"><span data-stu-id="c76fb-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="c76fb-112">Даже в том случае, если хранить сообщения поставщика никогда не уведомляет другие компоненты MAPI об изменениях в хранилище сообщений по-прежнему, он должен реализовывать **IMsgStore::Advise** для возврата MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c76fb-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c76fb-113">Эта информация указывает другим компонентам не ожидается, что поставщик хранилища уведомлений из сообщения.</span><span class="sxs-lookup"><span data-stu-id="c76fb-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c76fb-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c76fb-114">See also</span></span>



[<span data-ttu-id="c76fb-115">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="c76fb-115">Message Store Features</span></span>](message-store-features.md)

