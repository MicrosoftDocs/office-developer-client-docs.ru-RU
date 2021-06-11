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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит базовое имя файла библиотеки динамических ссылок поставщика служб MAPI (DLL).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Идентификатор:  <br/> |0x300A  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |MAPI общие  <br/> |
   
## <a name="remarks"></a>Примечания

MAPI использует конвенцию именования файлов DLL. Он применит строку 32 к базовому имени DLL, чтобы определить версию, которая выполняется на 32-битных платформах. Например, когда MAPI.DLL имя, MAPI строит имя MAPI32.DLL для представления соответствующей 32-битной версии DLL.
  
Эти свойства должны указывать базовое имя. MAPI применит строку 32 по мере необходимости. В том числе строка 32 в составе этого свойства приводит к ошибке.
  
## <a name="related-resources"></a>Связанные ресурсы

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

