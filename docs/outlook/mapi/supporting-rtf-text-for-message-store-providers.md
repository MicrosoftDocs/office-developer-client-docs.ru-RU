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
ms.openlocfilehash: 3e65ebd3ea485ca54978d622e8aaf093dc5eff74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594070"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Поддержка текста в формате RTF для поставщиков хранилищ сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Некоторые клиентские приложения позволяет пользователю использовать форматированный текст (RTF) текст в сообщения. Если сообщение хранения поставщика должно поддерживать текст RTF в сообщениях, он должен обрабатывать свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), в дополнение к свойству **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Прежде всего это означает, что хранения обоих свойств и проверьте, что **PR_BODY** содержит текстовая версия текста в **PR_RTF_COMPRESSED**. Функция [RTFSync](rtfsync.md) используется для этой цели. 
  
Существует два флаги, которые можно задать в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) объекта хранилища сообщений, которые сообщают клиентов, их можно ожидать от поставщика хранилища сообщений по отношению к **PR_BODY** и **PR_ RTF_COMPRESSED** свойства сообщения в хранилище сообщений. Флаг STORE_RTF_OK указывает, что хранилище можно создать значение свойства **PR_BODY** из свойства **PR_RTF_COMPRESSED** динамически, что уменьшает клиентов от необходимости их явным образом синхронизация. Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик хранения сообщений может поддерживать несжатую данных в **PR_RTF_COMPRESSED**.
  
Необходимо удалить свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), чтобы должным образом взаимодействовать с клиентскими приложениями, которые поддерживают текст RTF при изменении свойства **PR_BODY** поставщиков хранилища сообщений, которые не поддерживают текст RTF . 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

