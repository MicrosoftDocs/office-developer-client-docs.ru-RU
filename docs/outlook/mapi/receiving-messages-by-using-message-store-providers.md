---
title: Получение сообщений с помощью поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590192"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="40d69-103">Получение сообщений с помощью поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="40d69-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="40d69-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40d69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40d69-105">Могут не поддерживать входящих сообщений, отправляемых поставщиков хранилища сообщений (то есть, поддержка возможности поставщиками транспорта диспетчер очереди MAPI для использования сообщение удаленного хранилища и поставщика в качестве точки доставки сообщений).</span><span class="sxs-lookup"><span data-stu-id="40d69-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="40d69-106">Тем не менее если поставщик хранилища сообщений не поддерживает входящих сообщений, отправляемых, его нельзя использовать в качестве хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40d69-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="40d69-107">Чтобы обеспечить поддержку входящих сообщений, отправляемых, поставщиком хранилища сообщений необходимо выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="40d69-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="40d69-108">Поддерживает методы [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) и [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , поэтому клиентских приложений можно найти входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="40d69-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="40d69-109">Поддерживает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) , чтобы диспетчер очереди MAPI могут сообщить поставщика хранения сообщений, новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="40d69-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="40d69-110">Реализуйте уведомления, чтобы клиенты могут зарегистрировать для уведомление о получении сообщений.</span><span class="sxs-lookup"><span data-stu-id="40d69-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="40d69-111">Уведомления не являются обязательными, но их следует применить к поставщику.</span><span class="sxs-lookup"><span data-stu-id="40d69-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="40d69-112">Последовательность вызовов, происходит, когда входящее сообщение доставляется в хранилище сообщений выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40d69-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="40d69-113">Диспетчер очереди MAPI вызывает [IMsgStore::OpenEntry](imsgstore-openentry.md) с помощью папки «Входящие» [EntryID](entryid.md) для получения интерфейс [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="40d69-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="40d69-114">Диспетчер очереди MAPI вызывает [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для получения объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="40d69-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="40d69-115">Диспетчер очереди MAPI передает объект message поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="40d69-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="40d69-116">Поставщика транспорта заполняет свойств сообщений с данными системы обмена сообщениями и вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="40d69-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="40d69-117">Уведомление поставщика хранилища сообщений метод для оповещения зарегистрированных клиентов, новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="40d69-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="40d69-118">Диспетчер очереди MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="40d69-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="40d69-119">См. также</span><span class="sxs-lookup"><span data-stu-id="40d69-119">See also</span></span>



[<span data-ttu-id="40d69-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="40d69-120">Message Store Features</span></span>](message-store-features.md)

