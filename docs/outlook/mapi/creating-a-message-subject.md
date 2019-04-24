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
  
Тема сообщения, **пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)), является необязательным свойством, используемой для суммирования цели сообщения. Если выбрано значение, сделайте строку символов 128 байт или меньше. 128 байт не является предельным числом, накладываемым MAPI; Это ограничения, накладываемые некоторыми поставщиками хранилищ сообщений. Для обеспечения взаимодействия с поставщиками, которые накладывают его, ограничьте число субъектов до 128 байт. 
  
Обратите внимание, что некоторые поставщики хранилищ сообщений не разрешают **пр_субжект** запись в поток с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
  
Не задавайте **пр_субжект_префикс** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Это свойство задается только для ответов и переадресованных сообщений. 
  

