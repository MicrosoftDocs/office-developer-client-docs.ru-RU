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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит индекс, идентифицирующий один из набора предварительно определенных текстовых строк, связанных с флагом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидфлагстринженум  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x000085C0  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано, клиенты должны использовать соответствующее строковое значение в приведенных ниже таблицах (например, для замены строки, переведенной на язык текущего пользователя), и игнорировать значение, заданное в **диспидфлагрекуест** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) и **диспидвалидфлагстрингпруф** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Для объектов Contact можно указать следующие значения по умолчанию:
  
|**Значение**|**Строка на английском языке**|
|:-----|:-----|
|0x00000000 или отсутствует  <br/> | Следуйте указаниям, связанным с отображением **диспидфлагрекуест**.  <br/> |
|0x0000006E  <br/> |"К исполнению"  <br/> |
|0x0000006F  <br/> |Вызывать  <br/> |
|0x00000070  <br/> |"Упорядочить собрание"  <br/> |
|0x00000071  <br/> |"Отправить электронную почту"  <br/> |
|0x00000072  <br/> |"Отправить письмо"  <br/> |
   
По умолчанию для всех других объектов сообщений предлагается следующее:
  
|**Значение**|**Строка на английском языке**|
|:-----|:-----|
|0x00000000 или отсутствует  <br/> | Следуйте указаниям, связанным с отображением **диспидфлагрекуест**.  <br/> |
|0x00000001  <br/> |Вызывать  <br/> |
|0x00000002  <br/> |"Не пересылать"  <br/> |
|0x00000003  <br/> |"К исполнению"  <br/> |
|0x00000004  <br/> |"Для получения сведений"  <br/> |
|0x00000005  <br/> |"Forward" («Переслать»)  <br/> |
|0x00000006  <br/> |"Нет ответа не требуется"  <br/> |
|0x00000007  <br/> |Прочитан  <br/> |
|0x00000008  <br/> |"Reply" («Ответить»)  <br/> |
|0x00000009  <br/> |"Ответить всем"  <br/> |
|0x0000000A  <br/> |Смотрите  <br/> |
   
Все указанные выше строки можно перевести на язык пользователя, если это необходимо.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

