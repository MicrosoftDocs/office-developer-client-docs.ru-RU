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
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Предоставление отчетов о прочтении и непрочтении для поставщиков хранилищ сообщений

  
  
**Относится к**: Outlook 
  
Если поставщик хранения сообщения можно получать сообщения, необходимые для поддержки чтения и nonread отчетами сообщений, полученных поставщиком хранилища сообщений. Если получено сообщение содержит свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и значение этого свойства имеет значение TRUE, при открытии сообщения, хранилище сообщений необходимо отправить сообщение уведомления отправителя Указывает, что о сообщениях. Аналогично Если пользователь удаляет сообщение перед открытием, хранилища сообщений следует заключать ее в ответ отправителю, указывающего на то, что сообщение не было прочитано.
  
Выдача этих отчетов заключается в создании [IMessage: IMAPIProp](imessageimapiprop.md) объекта заполнения соответствующих свойств в окне сообщения и отправки для очереди MAPI, как если было создано сообщение с этим пользователем. Для этого можно использовать метод [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) . 
  
> [!NOTE]
> Специальные необходимо соблюдать осторожность при хранилища сообщений копии непрочитанные сообщения с ожидающими чтения или nonread отчеты. Не следует создавать таких отчетов при пользователи читать все копии сообщения, для которого запрошенные отчеты. При создании копии такого сообщения, поставщик хранения сообщение должно содержать флаги CLEAR_RN_PENDING и CLEAR_NRN_PENDING в его вызовы [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) и [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

