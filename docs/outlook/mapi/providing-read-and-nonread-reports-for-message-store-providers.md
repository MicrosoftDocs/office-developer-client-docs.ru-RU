---
title: Предоставление отчетов о прочтении и непрочтении для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812115"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="e3643-103">Предоставление отчетов о прочтении и непрочтении для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="e3643-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="e3643-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3643-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3643-105">Если поставщик хранения сообщения можно получать сообщения, необходимые для поддержки чтения и nonread отчетами сообщений, полученных поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e3643-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="e3643-106">Если получено сообщение содержит свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и значение этого свойства имеет значение TRUE, при открытии сообщения, хранилище сообщений необходимо отправить сообщение уведомления отправителя Указывает, что о сообщениях.</span><span class="sxs-lookup"><span data-stu-id="e3643-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="e3643-107">Аналогично Если пользователь удаляет сообщение перед открытием, хранилища сообщений следует заключать ее в ответ отправителю, указывающего на то, что сообщение не было прочитано.</span><span class="sxs-lookup"><span data-stu-id="e3643-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="e3643-108">Выдача этих отчетов заключается в создании [IMessage: IMAPIProp](imessageimapiprop.md) объекта заполнения соответствующих свойств в окне сообщения и отправки для очереди MAPI, как если было создано сообщение с этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="e3643-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="e3643-109">Для этого можно использовать метод [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) .</span><span class="sxs-lookup"><span data-stu-id="e3643-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e3643-110">Специальные необходимо соблюдать осторожность при хранилища сообщений копии непрочитанные сообщения с ожидающими чтения или nonread отчеты.</span><span class="sxs-lookup"><span data-stu-id="e3643-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="e3643-111">Не следует создавать таких отчетов при пользователи читать все копии сообщения, для которого запрошенные отчеты.</span><span class="sxs-lookup"><span data-stu-id="e3643-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="e3643-112">При создании копии такого сообщения, поставщик хранения сообщение должно содержать флаги CLEAR_RN_PENDING и CLEAR_NRN_PENDING в его вызовы [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) и [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="e3643-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3643-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e3643-113">See also</span></span>



[<span data-ttu-id="e3643-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="e3643-114">Message Store Features</span></span>](message-store-features.md)

