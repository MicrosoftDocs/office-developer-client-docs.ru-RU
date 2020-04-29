---
title: Поддержка текста в формате RTF для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414216"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Поддержка текста в формате RTF для поставщиков хранилищ сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Некоторые клиентские приложения позволяют пользователям использовать текст в формате RTF в своих сообщениях. Если поставщик хранилища сообщений должен поддерживать Текст RTF в сообщениях, необходимо обработать свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в дополнение к свойству **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). В основном это означает хранение обоих свойств и обеспечение того, что **PR_BODY** содержит текстовую версию текста в **PR_RTF_COMPRESSED**. Для этой цели удобно использовать функцию [ртфсинк](rtfsync.md) . 
  
Существует два флага, которые можно задать в свойстве **PR_STORE_SUPPORT_MASK** объекта хранилища сообщений ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), которые сообщают клиентам, что они могут ожидать от поставщика хранилища сообщений относительно свойств **PR_BODY** и **PR_RTF_COMPRESSED** в сообщениях в хранилище сообщений. Флаг STORE_RTF_OK указывает на то, что хранилище может динамически создавать значение свойства **PR_BODY** из свойства **PR_RTF_COMPRESSED** , что освобождает клиенты от нагрузки для их синхронизации явным образом. Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик хранилища сообщений может поддерживать несжатые данные в **PR_RTF_COMPRESSED**.
  
Поставщики хранилищ сообщений, не поддерживающие текст RTF, должны удалить свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) при изменении свойства **PR_BODY** , чтобы обеспечить правильное взаимодействие с клиентскими приложениями, поддерживающими текст RTF. 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

