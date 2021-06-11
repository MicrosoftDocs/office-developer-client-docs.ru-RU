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
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332965"
---
# <a name="creating-a-message-subject"></a>Создание темы сообщения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Тема сообщения, **PR_SUBJECT** [(PidTagSubject),](pidtagsubject-canonical-property.md)является необязательным свойством, используемым для обобщения намерения сообщения. Если вы решите установить его, сделайте его строкой символов 128 bytes или меньше. Ограничение в 128 byte не является ограничением, введенным MAPI; это ограничение, введенное некоторыми поставщиками магазинов сообщений. Для обеспечения связи с поставщиками, которые налагают его, ограничите количество субъектов 128 bytes. 
  
Следует помнить, что некоторые поставщики  хранения сообщений не позволяют PR_SUBJECT в поток с интерфейсом [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
  
Не **задай PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix);](pidtagsubjectprefix-canonical-property.md) это свойство задалось только для ответов и переададных сообщений. 
  

