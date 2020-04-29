---
title: Раздел "файл конфигурации формы [расширения]"
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
# <a name="form-configuration-file-extensions-section"></a>Раздел "файл конфигурации формы [расширения]"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В разделе **[Extensions]** перечисляются расширенные атрибуты формы, обычно это именованный набор свойств, который содержит все атрибуты за пределами базовых, перечисленных в разделе **[Description]** файла конфигурации формы. Расширенные атрибуты — это свойства, возвращаемые из вызовов метода **PROPS** объекта **имапиформинфо** с набором High bit в теге Property. Клиентские приложения могут определять дополнительные атрибуты формы, если они есть, путем извлечения этих тегов. Для этого клиенты вызывают метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , передавая имена свойств формы и вызывайте метод [IMAPIProp:: Prop](imapiprop-getprops.md) для получения свойств. 
  
 **Разрешений**
  
 **Модулей.** _строка1_ =  _строка2_
  
Каждый раздел свойства расширения определяет один атрибут расширения с помощью синтаксиса именованного свойства MAPI. Типом свойства должен быть либо PT_LONG, либо PT_STRING8. Наборы свойств, содержащие именованные строки, не поддерживаются. Формат раздела **[Extension]** : 
  
 **Модулей.** _строка2_ **]**
  
 **Тип** =  _Integer_
  
 **NmidPropset** =  _GUID_ нмидпропсет
  
 **NmidInteger** =  _Целое число_ нмидинтежер
  
 **Value** =  _string_Строка |  значения_Integer_
  
Ниже приведен пример раздела **[Extensions]** и последующих связанных разделов. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


