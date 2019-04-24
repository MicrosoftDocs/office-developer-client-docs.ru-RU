---
title: Предоставление отчетов о проЧтении и непрочтении для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328513"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="34335-103">Предоставление отчетов о проЧтении и непрочтении для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="34335-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="34335-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34335-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34335-105">Если поставщик хранилища сообщений может получать сообщения, он должен поддерживать отчеты о прочтении и отчеты о непрочтенных сообщениях, получаемых поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="34335-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="34335-106">Если полученное сообщение содержит свойство **пр_реад_рецеипт_рекуестед** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)), а значение этого свойства равно true, то при открытии сообщения в хранилище сообщений необходимо отправить уведомление отправителю. Указывает, что сообщение прочитано.</span><span class="sxs-lookup"><span data-stu-id="34335-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="34335-107">Аналогичным образом, если пользователь удаляет сообщение перед его открытием, то хранилище сообщений должно отправить ответ отправителю, указывая, что сообщение не было прочитано.</span><span class="sxs-lookup"><span data-stu-id="34335-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="34335-108">ВыПолнив эти отчеты, вы можете создать объект [iMessage: IMAPIProp](imessageimapiprop.md) , заполняя соответствующие свойства сообщения и отправив его в Диспетчер очереди MAPI так, как если бы сообщение поступило от пользователя.</span><span class="sxs-lookup"><span data-stu-id="34335-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="34335-109">Для этого можно использовать метод [имаписуппорт:: ReadReceipt](imapisupport-readreceipt.md) .</span><span class="sxs-lookup"><span data-stu-id="34335-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="34335-110">Если хранилище сообщений создает копии непрочитанного сообщения с непрочитанными или непрочтенными отчетами, необходимо принять специальные меры.</span><span class="sxs-lookup"><span data-stu-id="34335-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="34335-111">Такие отчеты не должны создаваться при чтении пользователями копий сообщений, для которых были запрошены отчеты.</span><span class="sxs-lookup"><span data-stu-id="34335-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="34335-112">При создании копии такого сообщения поставщик хранилища сообщений должен содержать флаги КЛЕАР_РН_ПЕНДИНГ и КЛЕАР_НРН_ПЕНДИНГ в вызовах [IMAPIFolder:: сетреадфлагс](imapifolder-setreadflags.md) и [iMessage:: сетреадфлаг](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="34335-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34335-113">См. также</span><span class="sxs-lookup"><span data-stu-id="34335-113">See also</span></span>



[<span data-ttu-id="34335-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="34335-114">Message Store Features</span></span>](message-store-features.md)

