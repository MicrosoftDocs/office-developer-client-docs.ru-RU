---
title: Создание темы сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cae255b90e8f2ccaaec4736c7ba1e9d6b7764f58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593111"
---
# <a name="creating-a-message-subject"></a>Создание темы сообщения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Тема сообщения, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — это необязательное свойство, используемый для суммирования смыслу сообщение. Если выбрано задание его, сделать его строку знаков 128 байт или меньше. Ограничение 128 байтов не предела, накладываемого оператором MAPI; Это ограничения, налагаемые некоторых поставщиков хранилища сообщений. Чтобы обеспечить взаимодействие с поставщиками, указывающие его, ограничьте субъектам 128 байт. 
  
Обратите внимание, что некоторые поставщики хранения сообщения не разрешать **PR_SUBJECT** для записи потока с помощью интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
Не используйте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Это свойство задавать только для ответов и пересылки сообщений. 
  

