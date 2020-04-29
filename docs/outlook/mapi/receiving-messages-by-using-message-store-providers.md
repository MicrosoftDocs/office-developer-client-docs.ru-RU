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
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418731"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="b52bf-103">Получение сообщений с помощью поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="b52bf-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="b52bf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b52bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b52bf-105">Поставщикам хранилищ сообщений не требуется поддержка отправки входящих сообщений (то есть, поддержка поставщиков транспорта и диспетчера очереди MAPI для использования поставщика хранилища сообщений в качестве точки доставки для сообщений).</span><span class="sxs-lookup"><span data-stu-id="b52bf-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="b52bf-106">Тем не менее, если поставщик хранилища сообщений не поддерживает отправки входящих сообщений, его нельзя использовать в качестве хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b52bf-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="b52bf-107">Для поддержки отправки входящих сообщений поставщик хранилища сообщений должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b52bf-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="b52bf-108">Поддерживает методы [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) и [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) , чтобы клиентские приложения могли находить входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="b52bf-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="b52bf-109">Поддерживает метод [IMsgStore:: нотифиневмаил](imsgstore-notifynewmail.md) , чтобы диспетчер очереди MAPI мог сообщить поставщику хранилища сообщений о поступлении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="b52bf-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="b52bf-110">Внедрять уведомления, чтобы клиенты могли регистрироваться на уведомления о новых сообщениях.</span><span class="sxs-lookup"><span data-stu-id="b52bf-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="b52bf-111">Уведомления являются необязательными, но поставщик должен их реализовать.</span><span class="sxs-lookup"><span data-stu-id="b52bf-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="b52bf-112">Последовательность вызовов методов, выполняемых при доставке входящего сообщения в хранилище сообщений, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b52bf-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="b52bf-113">Диспетчер очереди MAPI вызывает [IMsgStore:: OpenEntry](imsgstore-openentry.md) с идентификатором папки ["](entryid.md) Входящие" для получения интерфейса [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="b52bf-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="b52bf-114">Диспетчер очереди MAPI вызывает метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для получения нового объекта Message.</span><span class="sxs-lookup"><span data-stu-id="b52bf-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="b52bf-115">Диспетчер очереди MAPI передает объект Message поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="b52bf-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="b52bf-116">Поставщик транспорта заполняет свойства сообщения данными из базовой системы обмена сообщениями и вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) объекта Message.</span><span class="sxs-lookup"><span data-stu-id="b52bf-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="b52bf-117">Поставщик хранилища сообщений использует метод уведомления, чтобы уведомить зарегистрированных клиентов о поступлении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="b52bf-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="b52bf-118">Диспетчер очереди MAPI вызывает метод [IMsgStore:: нотифиневмаил](imsgstore-notifynewmail.md) хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b52bf-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b52bf-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b52bf-119">See also</span></span>



[<span data-ttu-id="b52bf-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="b52bf-120">Message Store Features</span></span>](message-store-features.md)

