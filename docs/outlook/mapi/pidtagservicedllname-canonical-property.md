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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя файла DLL, содержащего функцию точки входа поставщика службы сообщений для вызова конфигурации.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3D0A  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Когда имя функции точки входа отображается в методе **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName),](pidtagserviceentryname-canonical-property.md)оно указывает, что точка входа существует.
  
MAPI использует соглашение об именовостей файлов DLL. Он применит строку 32 к базовому имени DLL, чтобы определить версию, которая выполняется на 32-битных платформах. Например, если задан MAPI.DLL имя, MAPI MAPI32.DLL имя для представления соответствующей 32-битной версии DLL.
  
Эти свойства должны указывать базовое имя. MAPI при необходимости применит строку 32. Если строка 32 будет частью этих свойств, будет выявить ошибку.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

