---
title: Каноническое свойство PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810361"
---
# <a name="pidlidflagstring-canonical-property"></a>Каноническое свойство PidLidFlagString

  
  
**Относится к**: Outlook 
  
Содержит индекс, который определяет одну из набора предварительно определенных текстовых строк, связанных с флагом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFlagStringEnum  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000085C0  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Если задано это свойство, клиенты должны использовать соответствующее значение строки в таблице ниже (например, чтобы заменить строку, переведенный на язык текущего пользователя), а следует игнорировать значение, установленное в **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) и **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Доступны следующие параметры по умолчанию, предложенных пользователя для контактных объектов:
  
|**Значение**|**Строка на английском языке**|
|:-----|:-----|
|0x00000000 или отсутствует.  <br/> | Следуйте указаниям, связанные с отображением **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |«Исполнению»  <br/> |
|0x0000006F  <br/> |«Звонок»  <br/> |
|0x00000070  <br/> |«Упорядочить собрания»  <br/> |
|0x00000071  <br/> |«Отправка электронной почты»  <br/> |
|0x00000072  <br/> |«Отправлять письма»  <br/> |
   
Доступны следующие параметры по умолчанию, предложенных пользователей для всех других объектов сообщения:
  
|**Значение**|**Строка на английском языке**|
|:-----|:-----|
|0x00000000 или отсутствует.  <br/> | Следуйте указаниям, связанные с отображением **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |«Звонок»  <br/> |
|0x00000002  <br/> |«Не пересылать»  <br/> |
|0x00000003  <br/> |«Исполнению»  <br/> |
|0x00000004  <br/> |«К Вашему сведению»  <br/> |
|0x00000005  <br/> |«Вперед»  <br/> |
|0x00000006  <br/> |«Ответа не требуется»  <br/> |
|0x00000007  <br/> |«Чтение»  <br/> |
|0x00000008  <br/> |«Ответ»  <br/> |
|0x00000009  <br/> |«Ответить всем»  <br/> |
|0x0000000A  <br/> |«Обзор»  <br/> |
   
Все строки, указанных выше может быть переведено на язык пользователя при необходимости.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

