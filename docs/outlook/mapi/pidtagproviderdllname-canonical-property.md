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
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811588"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Каноническое свойство PidTagProviderDllName

  
  
**Относится к**: Outlook 
  
Содержит имя базового файла библиотеки динамической компоновки поставщика служб MAPI (DLL).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Идентификатор:  <br/> |0x300A  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Распространенные MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

MAPI использует соглашение об именовании файл DLL. Базовое имя файла содержит до шести символов, которые однозначно идентифицируют библиотеки DLL. MAPI добавляет строку 32 базовое имя DLL-Библиотеку для идентификации версии, на котором работает на 32-разрядных платформ. Например, если имя MAPI. Указан DLL-Библиотеку, MAPI создает имя MAPI32. DLL-Библиотеку для представления соответствующих 32-разрядная версия библиотеки DLL.
  
Эти свойства следует указать базовое имя. MAPI добавляет строку 32 соответствующим образом. Как часть этого свойства приводит к ошибке, включая строку 32.
  
## <a name="related-resources"></a>Связанные ресурсы

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

