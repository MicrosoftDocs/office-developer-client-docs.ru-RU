---
title: Каноническое свойство PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432473"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Каноническое свойство PidTagServiceEntryName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя функции точки входа для настройки службы сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕРВИЦЕ_ЕНТРИ_НАМЕ  <br/> |
|Идентификатор:  <br/> |0x3D0B  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы разработчики службы сообщений предоставляли точку входа в службу сообщений, но точка входа не является обязательной. Однако точка входа должна быть указана только в том случае, если существуют связанные свойства конфигурации. Если эти свойства не существуют, MAPI предполагает, что точка входа не указана.
  
Библиотека динамической компоновки (DLL), в которой отображается функция точки входа, называется свойством **пр_сервице_длл_наме** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Для получения дополнительных сведений о точках входа в службу сообщений, ознакомьтесь со статьей [Реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Связанные ресурсы

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

