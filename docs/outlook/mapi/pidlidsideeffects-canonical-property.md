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
  
Управляет обработкой объекта сообщения клиентом при вводимых пользователем данных.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSideEffects  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008510  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Настройка времени запуска  <br/> |
   
## <a name="remarks"></a>Примечания

Необходимо установить по битовую или ноль или более следующих флагов.
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |При удалении объекта сообщения требуется дополнительная обработка.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Пользовательский интерфейс не связан с объектом сообщения.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |При перемещении или копировании объекта сообщения в объект папки с помощью свойства **PR_CONTAINER_CLASS** [(PidTagContainerClass)](pidtagcontainerclass-canonical-property.md)IPF требуется дополнительная обработка. Примечание".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |При копировании в другую папку для объекта сообщения требуется дополнительная обработка.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |При перемещении в другую папку для объекта сообщения требуется дополнительная обработка.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |При отобраке глаголов для пользователя требуется дополнительная обработка объекта сообщения.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Не удается отменить операцию удаления, ее не следует устанавливать, если не установлено "seOpenToDelete".  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Не удается отменить операцию копирования, ее не следует устанавливать, если не установлено "seOpenTocopy".  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Не удается отменить операцию перемещения, ее не следует устанавливать, если не установлено "seOpenToMove".  <br/> |
|seHasScript  <br/> |0x2000  <br/> |Объект сообщения содержит скрипт пользователя.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Для окончательного удаления объекта сообщения требуется дополнительная обработка.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

