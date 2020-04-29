---
title: Каноническое свойство PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331299"
---
# <a name="pidlidsideeffects-canonical-property"></a>Каноническое свойство PidLidSideEffects

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Управляет тем, как клиент обрабатывает объект Message при работе с пользовательским вводом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидсидиффектс  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008510  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Настройка времени выполнения  <br/> |
   
## <a name="remarks"></a>Примечания

Должно быть задано побитовое или ноль или более из следующих флагов.
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|сеопентоделете  <br/> |0x0001  <br/> |При удалении объекта Message необходимо выполнить дополнительную обработку объекта Message.  <br/> |
|сенофраме  <br/> |0x0008  <br/> |С объектом Message не связан пользовательский интерфейс.  <br/> |
|секоерцетоинбокс  <br/> |0x0010  <br/> |Для объекта Message требуется дополнительная обработка при перемещении или копировании в объект Folder с помощью свойства **PR_CONTAINER_CLASS** ([PIDTAGCONTAINERCLASS](pidtagcontainerclass-canonical-property.md)) "IPF. Note (Примечание).  <br/> |
|сеопентокопи  <br/> |0x0020  <br/> |При копировании в другую папку требуется дополнительная обработка объекта Message.  <br/> |
|сеопентомове  <br/> |0x0040  <br/> |При перемещении в другую папку требуется дополнительная обработка объекта Message.  <br/> |
|сеопенфорктксмену  <br/> |0x0100  <br/> |При отображении команд для конечного пользователя требуется дополнительная обработка объекта Message.  <br/> |
|секаннотундоделете  <br/> |0x0400  <br/> |Невозможно отменить операцию удаления, если не задано значение "Сеопентоделете".  <br/> |
|секаннотундокопи  <br/> |0x0800  <br/> |Невозможно отменить операцию копирования, если не задано значение "Сеопентокопи".  <br/> |
|секаннотундомове  <br/> |0x1000  <br/> |Невозможно отменить операцию перемещения, если не задано значение "Сеопентомове".  <br/> |
|сехасскрипт  <br/> |0x2000  <br/> |Объект Message содержит скрипт конечного пользователя.  <br/> |
|сеопентопермделете  <br/> |0x4000  <br/> |Для окончательного удаления объекта Message требуется дополнительная обработка.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определение набора свойств и ссылки на соответствующие спецификации протокола Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

