---
title: Каноническое свойство PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330067"
---
# <a name="pidtagservicedllname-canonical-property"></a>Каноническое свойство PidTagServiceDllName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя библиотеки DLL, содержащей функцию точки входа поставщика службы сообщений, которую необходимо вызвать для настройки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ, ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ_А, ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x3D0A  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Если имя функции в точке входа присутствует в методе **пр_сервице_ентри_наме** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), оно указывает, что точка входа существует.
  
MAPI использует соглашение об именовании файлов DLL. Он добавляет к имени базового DLL строку 32, чтобы определить версию, работающую на 32 разрядных платформах. Например, если имя MAPI. DLL, то MAPI создает имя MAPI32. DLL для представления соответствующей 32 разрядной версии DLL.
  
Эти свойства должны указывать базовое имя. MAPI добавляет строку 32 в соответствии с требованиями. Включение строки 32 в состав этих свойств приводит к ошибке.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

