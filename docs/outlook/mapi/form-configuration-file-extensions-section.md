---
title: Файл конфигурации формы [расширения] Раздел
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423757"
---
# <a name="form-configuration-file-extensions-section"></a>Файл конфигурации формы [расширения] Раздел

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В разделе **[Extensions]** перечислены расширенные атрибуты формы, как правило, именоватый набор свойств, которые являются атрибутами, которые выходят за пределы базовых атрибутов, перечисленных в разделе **[Описание]** файла конфигурации формы. Расширенные атрибуты — это свойства, возвращаемые при вызовах метода **GetProps** объекта **IMAPIFormInfo** с высоким битом в теге свойства. Клиентские приложения могут определять расширенные атрибуты формы (если они есть) с помощью этих тегов. Для этого клиенты вызовите метод [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) передав имена свойств формы и вызовите метод [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить свойства. 
  
 **[Расширения]**
  
 **Расширение.** _string1_  =   _string2_
  
В каждом разделе свойств расширения определяется один атрибут расширения с использованием синтаксиса именуемой свойства MAPI. Тип свойства должен быть PT_LONG или PT_STRING8. Наборы свойств, которые содержат именуемую строку, не поддерживаются. Формат раздела **[Расширение]:** 
  
 **[Расширение.** _string2_ **]**
  
 **Тип**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidInteger**  =   _integer_
  
 **Значение**  =   _string_  |   _integer_
  
Ниже показан пример **раздела [Расширения]** и последующего связанного раздела. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


