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
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357787"
---
# <a name="pidlidflagstring-canonical-property"></a>Каноническое свойство PidLidFlagString

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит индекс, который определяет одну из наборов заранее определенных текстовых строк, связанных с флагом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFlagStringEnum  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085C0  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано, клиенты должны использовать соответствующее значение строки в таблицах ниже (например, заменить строку, переведенную на язык текущего пользователя), и игнорировать значение, заданное в **dispidFlagRequest** [(PidLidFlagRequest)](pidlidflagrequest-canonical-property.md)и **dispidValidFlagStringProof** [(PidLidValidFlagStringProof).](pidlidvalidflagstringproof-canonical-property.md) 
  
По умолчанию, предложенные пользователю для контактных объектов:
  
|**Значение**|**Английская строка**|
|:-----|:-----|
|0x00000000 или нет  <br/> | Следуйте указаниям, связанным с отображением **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Follow up"  <br/> |
|0x0000006F  <br/> |"Вызов"  <br/> |
|0x00000070  <br/> |"Организовать собрание"  <br/> |
|0x00000071  <br/> |"Отправка электронной почты"  <br/> |
|0x00000072  <br/> |"Отправить письмо"  <br/> |
   
По умолчанию, предложенные пользователю для всех остальных объектов сообщений, выполните следующим образом:
  
|**Значение**|**Английская строка**|
|:-----|:-----|
|0x00000000 или нет  <br/> | Следуйте указаниям, связанным с отображением **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |"Вызов"  <br/> |
|0x00000002  <br/> |"Не переад.  <br/> |
|0x00000003  <br/> |"Follow up"  <br/> |
|0x00000004  <br/> |"Для ваших сведений"  <br/> |
|0x00000005  <br/> |"Forward" («Переслать»)  <br/> |
|0x00000006  <br/> |"Не требуется ответа"  <br/> |
|0x00000007  <br/> |"Чтение"  <br/> |
|0x00000008  <br/> |"Reply" («Ответить»)  <br/> |
|0x00000009  <br/> |"Ответ на все"  <br/> |
|0x0000000A  <br/> |"Обзор"  <br/> |
   
Все строки, указанные выше, при необходимости могут быть переведены на язык пользователя.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

