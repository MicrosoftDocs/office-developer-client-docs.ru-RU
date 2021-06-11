---
title: Получение сообщений с помощью поставщиков магазинов сообщений
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
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="d55fd-103">Получение сообщений с помощью поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="d55fd-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="d55fd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d55fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d55fd-105">Поставщики магазинов сообщений не должны поддерживать входящие сообщения (то есть поддерживать возможность поставщиков транспорта и пулера MAPI использовать поставщика магазина сообщений в качестве точки доставки сообщений).</span><span class="sxs-lookup"><span data-stu-id="d55fd-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="d55fd-106">Однако если поставщик магазина сообщений не поддерживает входящие сообщения, его нельзя использовать в качестве магазина сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d55fd-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="d55fd-107">Чтобы поддерживать входящие сообщения, поставщик магазина сообщений должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="d55fd-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="d55fd-108">Поддержка [методов IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) и [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы клиентские приложения могли находить входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="d55fd-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="d55fd-109">Поддержив [метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) вы можете сообщить поставщику магазина сообщений о том, что пришло новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="d55fd-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="d55fd-110">Реализация уведомлений, чтобы клиенты могли зарегистрироваться для нового уведомления о сообщении.</span><span class="sxs-lookup"><span data-stu-id="d55fd-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="d55fd-111">Уведомления необязательны, но поставщик должен их реализовать.</span><span class="sxs-lookup"><span data-stu-id="d55fd-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="d55fd-112">Последовательность вызовов метода, которая возникает при доставке входящих сообщений в хранилище сообщений, является следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d55fd-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="d55fd-113">Spooler MAPI вызывает [IMsgStore::OpenEntry](imsgstore-openentry.md) с [](entryid.md) входной записью Входящие, чтобы получить [интерфейс IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="d55fd-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="d55fd-114">Spooler MAPI вызывает [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md) чтобы получить новый объект сообщения.</span><span class="sxs-lookup"><span data-stu-id="d55fd-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="d55fd-115">Шпалер MAPI передает объект сообщения поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="d55fd-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="d55fd-116">Поставщик транспорта заполняет свойства сообщения данными из системы обмена сообщениями и вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="d55fd-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="d55fd-117">Поставщик магазина сообщений использует метод уведомления для информирования зарегистрированных клиентов о том, что пришло новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="d55fd-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="d55fd-118">Spooler MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="d55fd-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d55fd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d55fd-119">See also</span></span>



[<span data-ttu-id="d55fd-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="d55fd-120">Message Store Features</span></span>](message-store-features.md)

