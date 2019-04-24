---
title: Файл конфигурации формы — раздел [Verbs]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327498"
---
# <a name="form-configuration-file-verbs-section"></a>Файл конфигурации формы — раздел [Verbs]

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В разделе **[Verbs]** приводится полный набор команд, поддерживаемых формой. Формат раздела **[Verbs]** : 
  
 **Команд**
  
 **** =  _Строка_ Verb1
  
Ниже приведен пример раздела **[Verbs]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Каждая команда определена в отдельной **[verb.** _строка_ **]** раздел. **[Verb.** _строка_ **]** в разделе описывается одна команда, предлагаемая формой. Запись **DisplayName** в **[verb.** _строка_ **]** раздел указывает имя команды, отображаемое в пользовательском интерфейсе. Запись **кода** соответствует номеру команды, переданному в методе [Имапиформ::D оверб](imapiform-doverb.md) . Синтаксис **[verb.** _строка_ **]** раздел: 
  
 **Команд.** _строка_ **]**
  
 **** =  _Отображаемая строка_ DisplayName
  
 **** =  _Целое число_ кода
  
 **** =  _Целое число_ флагов
  
 **** =  _Целое число_ аттрибс
  
Ниже приведен пример **[verb.** _строка_ **]** раздел. 
  
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

Команды, перечисленные в этом разделе, извлекаются клиентом с помощью [метода имапиформинфо:: калквербсет](imapiforminfo-calcverbset.md). Команды активируются, вызывая метод формы [имапиформ::D оверб](imapiform-doverb.md) и передавая ему номер кода выполняемой команды. 
  

