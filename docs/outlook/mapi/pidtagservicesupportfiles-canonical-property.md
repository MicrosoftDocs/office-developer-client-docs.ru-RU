---
title: Каноническое свойство PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811945"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Каноническое свойство PidTagServiceSupportFiles

  
  
**Относится к**: Outlook 
  
Содержит список файлов, относящихся к службе сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Идентификатор:  <br/> |0x3D0F  <br/> |
|Тип данных:  <br/> |PT_MV_STRING8 PT_MV_UNICODE  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Используя диалоговое окно "" в панели управления, пользователь может получить список файлов, относящихся к службе сообщений. Например пользователь может получить имена все библиотеки динамической компоновки (DLL), относящихся к службе. Пользователь затем может выполнять поиск дополнительных сведений об указанных файлов, таких как имена и номера версий всех библиотек DLL. MAPI использует эти свойства, чтобы создать список файлов поддержки в диалоговом окне Выбор пользователей системы обмена сообщениями.
  
MAPI для работы только с имена файлов и другие строки, переданным в него, в наборе символов интерфейсов службы Active Directory (ANSI). Клиентские приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.
  
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

