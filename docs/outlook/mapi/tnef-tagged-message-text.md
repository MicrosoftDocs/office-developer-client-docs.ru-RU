---
title: Текст сообщения с тегами TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812493"
---
# <a name="tnef-tagged-message-text"></a>Текст сообщения с тегами TNEF

  
  
**Относится к**: Outlook 
  
Текст с тегами сообщения используется TNEF для устранения положения вложения в сообщении родительского. Это делается путем добавления заполнителя в качестве текста сообщения в позиции вложения. Заполнителя или вложения тег описывает вложение таким образом, что TNEF знает о разрешении вложение и положение. Теги форматируются следующим образом:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 ** \<Название объекта\> ** и ** \<имя файла\> ** являются переменными, содержащий значения, которые берутся из самого вложение. В тех случаях, где эти значения недоступны название по умолчанию в зависимости от типа вложения TNEF. 
  
** \<KeyNum\> ** переменная содержит текстовое представление ключа вложения, назначенный вложения с TNEF. Базовое значение ключа передается в вызов [OpenTnefStreamEx](opentnefstreamex.md) . Базовое значение не должно быть равно нулю и не должны быть одинаковыми для каждого вызова **OpenTnefStreamEx**. Должно быть достаточно для использования псевдо на основе системы времени из любой генератор случайных чисел, библиотека времени выполнения предоставляет, при условии, что гарантирует, что они не могут быть нулевой случайных чисел.
  
** \<Передачи имя\> ** переменная содержит либо потока имя передано [OpenTnefStreamEx](opentnefstreamex.md) звонок или значение свойства **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> Свойство **PR_ATTACH_TRANSPORT_NAME** и ** \<передачи имя\> ** переменной в теге текста сообщения не работают с именем реализации поставщика транспорта. Эти элементы представляют имя вложения для поставщика транспорта и системы обмена сообщениями. 
  
Текст сообщения является меткой при поставщика транспорта запрашивает текст с тегами сообщения путем вызова метода [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . При чтении из потока текст с тегами TNEF заменяет один символ, который был в качестве текста сообщения по индексу, представленные в свойстве **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) с помощью соответствующего тега. При записи в поток текста с тегами TNEF проверяет входные данные для тегов, находит связанное вложение и заменяет тега одним пробелом.
  
Обратите внимание на то, что с помощью текст с тегами сообщения, поставщика транспорта можно сохранить размещение вложения независимо от того, большинство изменений, внесенных в текст сообщения систем обмена сообщениями.
  
