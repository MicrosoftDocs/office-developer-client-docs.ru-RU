---
title: Каноническое свойство PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282363"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Каноническое свойство PidTagAdditionalRenEntryIds

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификаторы определенных специальных папок. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АДДИТИОНАЛ_РЕН_ЕНТРИДС  <br/> |
|Идентификатор:  <br/> |0x36D8  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Приложение Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

Первые пять записей этого многозначного свойства применяются к следующим особым папкам, если они существуют в хранилище:
  
0 — папка конфликтов
  
1 — папка "ошибки синхронизации"
  
2 — папка "Локальные ошибки"
  
3 — папка "ошибки сервера"
  
4 — Папка нежелательной почты
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.
    
[[MS — ОКСФИШ]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Определяет и помечает сообщения электронной почты, предназначенные для получения пользователями конфиденциальных сведений (таких как пароли и другие персональные данные) в ненадежном источнике.
    
[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заГоловков

Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


[Сведения об API хранилищ](https://msdn.microsoft.com/library/aa192884.aspx)

