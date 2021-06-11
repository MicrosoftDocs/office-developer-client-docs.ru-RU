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
  
Указывает полную версию и создает сведения о Microsoft Exchange Server, к которым подключены учетные записи в профиле.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Идентификатор:  <br/> |0x663B  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Профиль может указать одну или несколько учетных записей, которые подключаются к Exchange Server, но они должны быть подключены к одному Exchange Server.
  
Версии Outlook более ранних Microsoft Office Outlook 2007 года не поддерживают это свойство. Для этих версий Outlook проверьте наличие PR_PROFILE_SERVER_VERSION **[в](pidtagprofileserverversion-canonical-property.md)** профиле. 
  
Как правило, если активный почтовый ящик подключен к Exchange Server, Outlook 2007 г. Exchange Server  сведения о версии в свойстве PR_PROFILE_SERVER_FULL_VERSION в активном профиле. Outlook хранит сведения в структуре **EXCHANGE_STORE_VERSION_NUM,** которая содержит основные и второстепенные номера версий, а также основные и второстепенные номера сборки. Например, чтобы сохранить идентификатор Exchange Server версии **8.0.685.24,** основной номер версии — 8, а второстепенный — 0, а основной номер сборки — 685, а число сборки — 24.
  
Только один **PR_PROFILE_SERVER_VERSION** **или PR_PROFILE_SERVER_FULL_VERSION** может существовать в профиле, но нет никакой гарантии, что либо всегда существует в профиле. Outlook не записыву в свойство, пока оно не будет успешно подключено к Exchange Server. 
  
В Outlook объектной модели можно использовать свойство **ExchangeMailboxServerVersion** объекта **NameSpace,** чтобы найти версию Exchange Server, на которой расположен активный почтовый ящик. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

