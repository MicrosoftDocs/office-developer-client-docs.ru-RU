---
title: Каноническое свойство PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286490"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Каноническое свойство PidTagProviderDllName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит базовое имя файла библиотеки динамической компоновки (DLL) поставщика службы MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A PR_PROVIDER_DLL_NAME_W  <br/> |
|Идентификатор:  <br/> |0x300A  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие протоколы MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

MAPI использует соглашение об именовании файлов DLL. Он добавляет к имени базового DLL строку 32, чтобы определить версию, работающую на 32 разрядных платформах. Например, если имя MAPI. DLL, то MAPI создает имя MAPI32. DLL для представления соответствующей 32 разрядной версии DLL.
  
Эти свойства должны указывать базовое имя. MAPI добавляет строку 32 в соответствии с требованиями. Включение строки 32 в качестве части этого свойства приводит к ошибке.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

