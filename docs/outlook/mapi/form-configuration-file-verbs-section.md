---
title: 'Файл конфигурации формы: раздел [Команды]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583976"
---
# <a name="form-configuration-file-verbs-section"></a>Файл конфигурации формы: раздел [Команды]

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
**[]** Разделе перечислены полный набор команд, поддерживаемых формы. Имеет формат **[]** разделе: 
  
 **[Команд]**
  
 **Verb1** =  _строки_
  
Ниже приведен пример раздела **[команд]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Команд определяется в отдельном **[глаголов.** _строка_ раздел **]** . A **[глаголов.** _строка_ **]** разделе описываются в виде одной команды. Запись **DisplayName** в **[глаголов.** _строка_ раздел **]** указывает имя команды, отображаемые в пользовательском интерфейсе. Запись **кода** соответствует номер команды, переданной в метод [IMAPIForm::DoVerb](imapiform-doverb.md) . Синтаксис для **[глаголов.** _строка_ раздел **]** : 
  
 **[Команда.** _строка_ **]**
  
 **Отображаемое имя** =  _отображается строка_
  
 **Код** =  _целое число_
  
 **Флаги** =  _целое число_
  
 **Атрибутов** =  _целое число_
  
Ниже приведен пример **[глаголов.** _строка_ раздел **]** . 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

Команды, приведенные в этом разделе извлекаются с помощью [метода IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)клиентом. Команды, активируются путем вызова метода [IMAPIForm::DoVerb](imapiform-doverb.md) формы и передав номер кода команды нужно выполнить. 
  

