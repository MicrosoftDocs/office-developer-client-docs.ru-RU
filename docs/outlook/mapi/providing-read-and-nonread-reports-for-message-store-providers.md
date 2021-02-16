---
title: Предоставление отчетов о прочтях и непрочитанных сообщениях для поставщиков store сообщений
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
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Предоставление отчетов о прочтях и непрочитанных сообщениях для поставщиков store сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если поставщик store сообщений может получать сообщения, он должен поддерживать отчеты о прочтях и непрочитанные сообщения, полученные поставщиком. Если полученное сообщение содержит свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested),](pidtagreadreceiptrequested-canonical-property.md)а значение этого свойства — TRUE, хранилище сообщений должно отправить отправителю уведомление, когда пользователь откроет сообщение, указывающее, что сообщение прочитано. Аналогично, если пользователь удаляет сообщение перед его открытием, хранилище сообщений должно отправить отправителю ответ, указывающий, что сообщение не было прочитано.
  
Создание этих отчетов — это создание объекта [IMessage : IMAPIProp,](imessageimapiprop.md) заполнение соответствующих свойств сообщения и его отправка в пул MAPI, как если бы сообщение было отправлено пользователем. Для этого можно использовать метод [IMAPISupport::ReadReceipt.](imapisupport-readreceipt.md) 
  
> [!NOTE]
> Особое внимание следует уделяем, если хранилище сообщений создает копии непрочитанные сообщения с ожидающих прочтевыми или непрочитаемыми отчетами. Такие отчеты не должны создаваться, когда пользователи читают какие-либо копии сообщения, для которого были запророшы отчеты. При создании копии такого сообщения поставщик хранилище сообщений должен включить флаги CLEAR_RN_PENDING и CLEAR_NRN_PENDING в свои вызовы [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) и [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

