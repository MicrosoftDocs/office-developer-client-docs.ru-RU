---
title: Каноническое свойство PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341953"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Каноническое свойство PidTagTnefCorrelationKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое сопоставляет вложение формата инкапсуляции (TNEF) с сообщением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Идентификатор:  <br/> |0x007F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы подобъекты Вложения TNEF выставили это свойство. Это свойство определяет, принадлежит ли входящий TNEF-файл сообщению, к нему присоединено. Он используется в основном поставщиками транспорта и шлюзами.
  
В исходящие сообщения поставщик транспорта должен вычислить двоичное значение, уникальное для этого сообщения, или использовать существующее значение, удовлетворяе требованиям уникальности, например идентификатор сообщения. Поставщик транспорта должен сохранить это значение в этом свойстве, а затем вызвать метод [ITnef::AddProps,](itnef-addprops.md) чтобы инкапсулировать его. Это же значение также должно храниться в транспортном конверте в месте, определенном поставщиком, например в загонах сообщений. 
  
В входящий сообщении поставщик транспорта должен вызвать метод [ITnef::ExtractProps,](itnef-extractprops.md) чтобы обезглавлить вложение TNEF, а затем сравнить это свойство со значением, сохраненным в транспортном конверте. Если значения совпадают, TNEF должен обрабатываться нормально, то есть все свойства, извлеченные из вложения TNEF, должны использоваться. Если значения не совпадают, все свойства вложения TNEF следует игнорировать. Если это свойство не установлено, файл TNEF должен считаться принадлежащим этому сообщению, а другие свойства, извлеченные из него, должны использоваться. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

