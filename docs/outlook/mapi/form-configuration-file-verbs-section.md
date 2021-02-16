---
title: Файл конфигурации формы [Verbs] Section
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
# <a name="form-configuration-file-verbs-section"></a>Файл конфигурации формы [Verbs] Section

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В **разделе [Verbs]** приводится полный набор глаголов, поддерживаемых формой. Формат раздела **[Verbs]:** 
  
 **[Verbs]**
  
 **Verb1**  =   _string_
  
Ниже приводится пример раздела **[Verbs].** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Каждая глагол определяется в **отдельном [Verb.** _строка_ **]** раздела. **[Verb.** _в_ разделе **строки** ] описывается одна глагол, предложенная формой. Запись **DisplayName** в **[Verb.** _В_ **разделе string ]** указывается имя команды, отображаемой в пользовательском интерфейсе. Запись **"Код"** соответствует номеру команды, передаемой в [методе IMAPIForm::D oVerb.](imapiform-doverb.md) Синтаксис **для [Verb.** _строка_ **]** раздел: 
  
 **[Verb.** _string_ **]**
  
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

Команды, перечисленные в этом разделе, извлекаются клиентом с помощью метода [IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md) Глаголы активируются путем вызова метода [IMAPIForm::D oVerb](imapiform-doverb.md) формы и передачи ему номера кода выполняемой команды. 
  

