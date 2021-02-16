---
title: Получение сообщений с помощью поставщиков store сообщений
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
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="38d8f-103">Получение сообщений с помощью поставщиков store сообщений</span><span class="sxs-lookup"><span data-stu-id="38d8f-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="38d8f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38d8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38d8f-105">Поставщики store сообщений не должны поддерживать отправку входящих сообщений (то есть поддерживают возможность поставщиков транспорта и пула MAPI использовать поставщика для хранения сообщений в качестве точки доставки сообщений).</span><span class="sxs-lookup"><span data-stu-id="38d8f-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="38d8f-106">Однако если поставщик вашего магазина сообщений не поддерживает отправку входящих сообщений, его нельзя использовать в качестве хранения сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38d8f-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="38d8f-107">Чтобы поддерживать отправку входящих сообщений, поставщик вашего магазина сообщений должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="38d8f-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="38d8f-108">Поддержка [методов IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) и [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы клиентские приложения могли находить входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="38d8f-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="38d8f-109">[Поддержив метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) вы можете сообщить поставщику хранилищ сообщений о том, что поступило новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="38d8f-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="38d8f-110">Реализуют уведомления, чтобы клиенты могли регистрироваться для нового уведомления о сообщении.</span><span class="sxs-lookup"><span data-stu-id="38d8f-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="38d8f-111">Уведомления необязательны, но поставщик должен их реализовать.</span><span class="sxs-lookup"><span data-stu-id="38d8f-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="38d8f-112">Последовательность вызовов метода, которые происходят при доставке входящих сообщений в хранилище сообщений:</span><span class="sxs-lookup"><span data-stu-id="38d8f-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="38d8f-113">Пулер MAPI вызывает [IMsgStore::OpenEntry](imsgstore-openentry.md) с inbox [EntryID](entryid.md) для получения [интерфейса IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="38d8f-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="38d8f-114">Пулер MAPI вызывает [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для получения нового объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="38d8f-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="38d8f-115">Пулер MAPI передает объект сообщения поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="38d8f-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="38d8f-116">Поставщик транспорта заполняет свойства сообщения данными из системы обмена сообщениями и вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="38d8f-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="38d8f-117">Поставщик банка сообщений использует свой метод уведомления, чтобы сообщить зарегистрированным клиентам о том, что поступило новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="38d8f-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="38d8f-118">Пулер MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="38d8f-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="38d8f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="38d8f-119">See also</span></span>



[<span data-ttu-id="38d8f-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="38d8f-120">Message Store Features</span></span>](message-store-features.md)

