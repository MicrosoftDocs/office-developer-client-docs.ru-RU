---
title: Раздел Конфигурация формы [Глаголы]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417786"
---
# <a name="form-configuration-file-verbs-section"></a>Раздел Конфигурация формы [Глаголы]

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В **разделе [Verbs]** перечислены полные наборы глаголов, поддерживаемых формой. Формат раздела **[Глаголы]:** 
  
 **[Глаголы]**
  
 **Verb1**  =   _строка_
  
Ниже приводится пример **раздела [Verbs].** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Каждый глагол определяется в **отдельном [Verb.** _строка_ **]** раздела. **[Глагол.** _строка_ **]** в разделе описывается один глагол, предлагаемый формой. Запись **DisplayName** в **[Verb.** _в_ разделе string **]** указывается имя команды, отображаемая в пользовательском интерфейсе. Запись **Кода** соответствует числу глаголов, переданным методом [IMAPIForm::D oVerb.](imapiform-doverb.md) Синтаксис **для [Verb.** _строка_ **]** раздел: 
  
 **[Глагол.** _строка_ **]**
  
 **DisplayName**  =   _отображаемая строка_
  
 **Код**  =   _integer_
  
 **Флаги**  =   _integer_
  
 **Attribs**  =   _integer_
  
Ниже приводится пример **[Verb.** _строка_ **]** раздела. 
  
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

Глаголы, перечисленные в этом разделе, извлекаются клиентом с помощью [метода IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md) Глаголы активируются, вызывая метод [IMAPIForm::D oVerb](imapiform-doverb.md) формы и передав ему кодовое число выполняемого глагола. 
  

