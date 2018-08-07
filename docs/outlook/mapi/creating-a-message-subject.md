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
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808249"
---
# <a name="creating-a-message-subject"></a>Создание темы сообщения

  
  
**Относится к**: Outlook 
  
Тема сообщения, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — это необязательное свойство, используемый для суммирования смыслу сообщение. Если выбрано задание его, сделать его строку знаков 128 байт или меньше. Ограничение 128 байтов не предела, накладываемого оператором MAPI; Это ограничения, налагаемые некоторых поставщиков хранилища сообщений. Чтобы обеспечить взаимодействие с поставщиками, указывающие его, ограничьте субъектам 128 байт. 
  
Обратите внимание, что некоторые поставщики хранения сообщения не разрешать **PR_SUBJECT** для записи потока с помощью интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
Не используйте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Это свойство задавать только для ответов и пересылки сообщений. 
  

