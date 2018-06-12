---
title: Раздел [команд] файла конфигурации формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808474"
---
# <a name="form-configuration-file-verbs-section"></a>Раздел [команд] файла конфигурации формы

  
  
**Применимо к**: Outlook 
  
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
  

