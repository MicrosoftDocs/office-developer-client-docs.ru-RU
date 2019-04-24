---
title: Каноническое свойство PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341603"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Каноническое свойство PidTagProfileServerFullVersion

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает полные сведения о версии и сборке сервера Microsoft Exchange, к которому подключены учетные записи в профиле.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРОФИЛЕ_СЕРВЕР_ФУЛЛ_ВЕРСИОН  <br/> |
|Идентификатор:  <br/> |0x663B  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Профиль может указывать одну или несколько учетных записей, которые подключаются к серверу Exchange Server, но должны быть подключены к одному и тому же серверу Exchange Server.
  
Более ранние версии Outlook, чем Microsoft Office Outlook 2007, не поддерживают это свойство. Для этих версий Outlook проверьте наличие **[пр_профиле_сервер_версион](pidtagprofileserverversion-canonical-property.md)** в профиле. 
  
Как правило, если активный почтовый ящик подключен к серверу Exchange Server, Outlook 2007 хранит сведения о версии Exchange Server в свойстве **пр_профиле_сервер_фулл_версион** в активном профиле. Outlook хранит информацию в структуре **ексчанже_сторе_версион_нум** , которая содержит основной и дополнительный номера версии, а также номера основной и вспомогательной сборок. Например, чтобы сохранить идентификатор версии сервера Exchange Server для **8.0.685.24**, основной номер версии равен 8, а дополнительный номер версии — 0, а номер основной сборки — 685, а дополнительный номер сборки — 24.
  
В профиле может существовать только один из **пр_профиле_сервер_версион** или **пр_профиле_сервер_фулл_версион** , но нет гарантии, что они всегда находятся в профиле. Outlook не выполняет запись в одно свойство, пока оно не будет успешно подключено к серверу Exchange Server. 
  
В объектной модели Outlook можно использовать свойство **ексчанжемаилбокссерверверсион** объекта **Namespace** , чтобы найти версию сервера Exchange Server, на котором размещается активный почтовый ящик. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Задает определения свойств.
    
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

