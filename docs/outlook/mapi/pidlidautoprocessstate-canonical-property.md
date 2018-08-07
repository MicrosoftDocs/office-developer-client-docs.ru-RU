---
title: Каноническое свойство PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810199"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>Каноническое свойство PidLidAutoProcessState

  
  
**Относится к**: Outlook 
  
Задает параметры, которые используются в автоматической обработки сообщений электронной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSniffState  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000851A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Свойство может отсутствовать, в противном случае используется значение по умолчанию «0x00000000». Если задано, это свойство должно быть присвоено одно из значений в таблице ниже.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Не обрабатывают сообщения автоматически.  <br/> |
|0x00000001  <br/> |Автоматически обрабатывать сообщения или при открытии сообщения.  <br/> |
|0x00000002  <br/> |Процесс сообщения только при открытии сообщения.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

