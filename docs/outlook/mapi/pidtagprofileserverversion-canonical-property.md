---
title: Каноническое свойство PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286568"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Каноническое свойство PidTagProfileServerVersion

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает сведения о версии Microsoft Exchange Server, к которой подключены учетные записи в профиле Outlook Майкрософт.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Идентификатор:  <br/> |0x661B  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Профиль может указать одну или несколько учетных записей, которые подключаются к Exchange Server, но они должны быть подключены к одному Exchange Server.
  
Версии Outlook до Microsoft Office Outlook 2007 г. могут записываться в это свойство для хранения сведений о версии Exchange Server, к которой подключен активный профиль. Однако формат сведений о версии зависит от различных версий Exchange Server. Например, Outlook в **PR_PROFILE_SERVER_VERSION** десятичной значение 6944 представляет только основной номер сборки в идентификаторе версии **6.5.6944.3** для Microsoft Exchange Server 2003 г. Для подключения Exchange 2007 Outlook сохраняет основной номер версии и основной номер сборки в одновременном гексадецимальной представлении этих номеров в свойстве. Идентификатор Exchange **версии 8.0.685.24 24** имеет основной номер версии 8 и основной сборки 685 в десятичной. Преобразование обоих номеров в гексадецимальные значения 0x8 и 0x2AD. Согласуя эти два номера, Outlook сохраняет значение 0x82AD в **PR_PROFILE_SERVER_VERSION** в гексадецимальной представлении. 
  
Outlook 2007 не читает и не записи в это свойство. Поддерживает **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

