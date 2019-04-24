---
title: Каноническое свойство PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316319"
---
# <a name="pidtagfoldertype-canonical-property"></a>Каноническое свойство PidTagFolderType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит константу, указывающую тип папки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ФОЛДЕР_ТИПЕ  <br/> |
|Идентификатор:  <br/> |0x3601  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только одно из следующих значений:
  
ФОЛДЕР_ЖЕНЕРИК 
  
> Общая папка, содержащая сообщения и другие папки.
    
ФОЛДЕР_РУТ 
  
> Корневая папка таблицы иерархии папок, то есть папка, не имеющая родительской папки.
    
ФОЛДЕР_СЕАРЧ 
  
> Папка, содержащая результаты поиска, в виде ссылок на сообщения, соответствующие условиям поиска.
    
Корневой каталог хранилища сообщений не следует путать с корневым деревом поддерева междоступного сообщения (IPM) в этом хранилище. Корневая папка хранилища, которая не имеет родителя, получается путем вызова метода [IMsgStore:: OpenEntry](imsgstore-openentry.md) с идентификатором записи null. Корневая папка поддерева IPM, у которой есть родитель, получается с помощью значения свойства **пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) для вызова **OpenEntry** . 
  
MAPI позволяет использовать только одну корневую папку для каждого хранилища сообщений. Эта папка содержит сообщения и другие папки. Свойство **пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) корневой папки содержит собственный идентификатор записи.
  
Сведения в папке результатов поиска в основном хранятся в таблице содержимого, которая содержит те же столбцы, что и обычная таблица содержимого, а также два лишних столбца, определяющих папку, в которой было найдено каждое сообщение: **пр_парент_дисплай** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (отображаемое имя, обязательное имя) и это свойство (идентификатор записи, необязательно).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

