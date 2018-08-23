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
ms.openlocfilehash: 79b6461ca4a796b292b86f0f3bdbd8a39ad65863
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575681"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Каноническое свойство PidTagProfileServerVersion

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает сведения о версии Microsoft Exchange Server, к которому подключены учетных записей в профиле Microsoft Outlook.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Идентификатор:  <br/> |0x661B  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Настройки профилей MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Профиль можно указать один или несколько учетных записей, которые подключаются к серверу Exchange, но они должна быть соединена с одного сервера Exchange.
  
Версии Outlook, предшествующие Microsoft Office Outlook 2007 можно создать для этого свойства для хранения сведений о версии Exchange Server, к которому подключен активного профиля. Тем не менее формат сведений о версии зависит от различных версий Exchange Server. Например Outlook хранилищ в **PR_PROFILE_SERVER_VERSION** десятичное значение 6944 для представления только основной номер в идентификатор версии **6.5.6944.3** сборки для Microsoft Exchange Server 2003. Для подключения к Exchange 2007 Outlook хранит основной номер версии и основной номер в составное шестнадцатеричное представление эти номера в свойстве построения. Идентификатор версии Exchange 2007 **8.0.685.24** имеет номер основной версии 8 и основной номер построения 685 в тип decimal. Преобразование обоих чисел в шестнадцатеричном представлении, вы получите 0x8 и 0x2AD. Объединения этих двух чисел, Outlook сохраняет значение 0x82AD в **PR_PROFILE_SERVER_VERSION** в шестнадцатеричном представлении. 
  
Outlook 2007 не чтение или запись с этим свойством. Поддержка **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Только один из **PR_PROFILE_SERVER_VERSION** или **PR_PROFILE_SERVER_FULL_VERSION** скорее всего, существуют в профиле, но не гарантируется, либо всегда существует в профиле. Outlook не записывает либо свойством только после успешного подключения к серверу Exchange. 
  
В объектной модели Outlook можно использовать свойство **ExchangeMailboxServerVersion** объекта **пространство имен** для поиска версии Exchange Server, на котором размещен почтовый ящик active. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

