---
title: Каноническое свойство PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810438"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Каноническое свойство PidLidOfflineStatus

  
  
**Относится к**: Outlook 
  
Определяет состояние файла на сервере, который реализует [MS-LISTSWS].
  
|||
|:-----|:-----|
|Связанными свойствами  <br/> |dispidOfflineStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000085B9  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

В следующей таблице показаны возможные значения этого свойства.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Документ не извлечен.  <br/> |
|1  <br/> |Документ извлечен текущим пользователем.  <br/> |
|2  <br/> |Документ не извлечен, но текущего пользователя имеется копия файл, сохраненный для редактирования на данном компьютере.  <br/> |
   
Это свойство рассчитывается локально и не отправляются на сервер в любое время, пока пользователь перетаскивает элемент в другую учетную запись. В этом случае он обрабатывается как пользовательские настраиваемого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

