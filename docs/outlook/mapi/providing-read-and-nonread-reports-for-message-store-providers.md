---
title: Предоставление отчетов о прочтях и непрочитанных данных для поставщиков магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432340"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="7903f-103">Предоставление отчетов о прочтях и непрочитанных данных для поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="7903f-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="7903f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7903f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7903f-105">Если поставщик хранения сообщений может получать сообщения, он должен поддерживать отчеты о прочтях и непрочитанные сообщения сообщений, полученных поставщиком магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="7903f-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="7903f-106">Если полученное сообщение содержит **свойство PR_READ_RECEIPT_REQUESTED** [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)и значение этого свойства является TRUE, магазин сообщений должен отправить сообщение уведомления отправителю, когда пользователь откроет сообщение, указав, что сообщение было прочитано.</span><span class="sxs-lookup"><span data-stu-id="7903f-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="7903f-107">Аналогичным образом, если пользователь удаляет сообщение перед его открытием, хранилище сообщений должно выдавать отправителю ответ, указывающий, что сообщение не было прочитано.</span><span class="sxs-lookup"><span data-stu-id="7903f-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="7903f-108">Выпуск этих отчетов — это создание объекта [IMessage : IMAPIProp,](imessageimapiprop.md) заполнение соответствующих свойств сообщения и отправка его в пульпер MAPI, как если бы сообщение возникло с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7903f-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="7903f-109">Для этого можно использовать метод [IMAPISupport::ReadReceipt.](imapisupport-readreceipt.md)</span><span class="sxs-lookup"><span data-stu-id="7903f-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7903f-110">Особое внимание следует уделять, когда хранилище сообщений создает копии непрочитанные сообщения с ожидаемыми отчетами о прочтевом или непрочитаемом.</span><span class="sxs-lookup"><span data-stu-id="7903f-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="7903f-111">Такие отчеты не должны создаваться, когда пользователи читают копии сообщения, для которого запрашивались отчеты.</span><span class="sxs-lookup"><span data-stu-id="7903f-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="7903f-112">При создании копии такого сообщения поставщик магазина сообщений должен включать флаги CLEAR_RN_PENDING и CLEAR_NRN_PENDING в вызовы [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) и [IMessage::SetReadFlags](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="7903f-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7903f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7903f-113">See also</span></span>



[<span data-ttu-id="7903f-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="7903f-114">Message Store Features</span></span>](message-store-features.md)

