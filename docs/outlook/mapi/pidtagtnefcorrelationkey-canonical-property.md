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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, сопоставляет вложение в формате TNEF с сообщением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Идентификатор:  <br/> |0x007F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы вложенные объекты Вложения TNEF выдали это свойство. Это свойство определяет, принадлежит ли входящий TNEF-файл сообщению, в которое оно вложено. В основном он используется поставщиками транспорта и шлюзами.
  
В исходящие сообщения поставщик транспорта должен вычислить уникальное для этого сообщения двоичное значение или использовать существующее значение, которое соответствует требованию уникальности, например идентификатор сообщения. Поставщик транспорта должен сохранить это значение в этом свойстве, а затем вызвать метод [ITnef::AddProps,](itnef-addprops.md) чтобы инкапсулировать его. Это же значение также должно храниться в конверте транспорта в месте, определенном поставщиком, например в заголке сообщения. 
  
В вложенном сообщении поставщик транспорта должен вызвать метод [ITnef::ExtractProps,](itnef-extractprops.md) чтобы декапсулировать Вложение TNEF, а затем сравнить это свойство со значением, сохраненным в конверте транспорта. Если значения совпадают, TNEF следует обрабатывать в обычном режиме, то есть использовать все свойства, извлеченные из вложения TNEF. Если значения не совпадают, все свойства из вложения TNEF следует игнорировать. Если это свойство не установлено, файл TNEF должен считаться принадлежащим этому сообщению, а также использовать другие извлеченные из него свойства. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

