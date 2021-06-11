---
title: Поддержка текста RTF для поставщиков магазинов сообщений
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
# <a name="supporting-rtf-text-for-message-store-providers"></a>Поддержка текста RTF для поставщиков магазинов сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Некоторые клиентские приложения позволяют пользователям использовать текст Rich Text Format (RTF) в своих сообщениях. Если поставщику хранения сообщений необходимо поддерживать текст RTF в сообщениях, ему необходимо обрабатывать свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)в дополнение к свойству **PR_BODY** [(PidTagBody).](pidtagbody-canonical-property.md) В первую очередь это означает хранение обоих свойств и обеспечение того, чтобы PR_BODY содержит простую текстовую версию текста в **PR_RTF_COMPRESSED**.  Функция [RTFSync](rtfsync.md) полезна для этой цели. 
  
В свойстве PR_STORE_SUPPORT_MASK объекта магазина сообщений [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)можно установить два флага, которые расскажут клиентам, чего они  могут ожидать от поставщика хранения сообщений в отношении свойств PR_BODY и **PR_RTF_COMPRESSED** сообщений в хранилище сообщений.  Флаг STORE_RTF_OK указывает, что хранилище может динамически генерировать  значение свойства PR_BODY  из свойства PR_RTF_COMPRESSED, что освобождает клиентов от нагрузки на их явное синхронизацию. Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик магазина сообщений может поддерживать незапечатаные данные **в PR_RTF_COMPRESSED**.
  
Поставщики магазинов сообщений, которые не поддерживают текст RTF, должны удалить свойство[PR_RTF_IN_SYNC (PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)при изменениях свойства PR_BODY, чтобы должным образом скооперироваться с клиентские приложения, поддерживают текст RTF.   
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

