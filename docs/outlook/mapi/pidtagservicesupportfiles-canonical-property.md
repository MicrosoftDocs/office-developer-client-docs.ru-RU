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
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417044"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Каноническое свойство PidTagServiceSupportFiles

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список файлов, принадлежащих службе сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Идентификатор:  <br/> |0x3D0F  <br/> |
|Тип данных:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Используя диалоговое окно в applet панели управления, пользователь может получить список файлов, принадлежащих службе сообщений. Например, пользователь может получить имена всех библиотек динамической ссылки, принадлежащих службе. Затем пользователь может получить дополнительные сведения об указанных файлах, например имена и номера версий всех DLL. MAPI использует эти свойства для создания списка файлов поддержки в диалоговом окне для выбора пользователя сообщений.
  
MAPI работает только с именами файлов и другими переданными ему строками в наборе символов интерфейсов службы Active Directory (ANSI). Клиентские приложения, которые используют имена файлов в наборе символов изготовителя оборудования (OEM), должны преобразовывать их в ANSI, прежде чем вызывать MAPI.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

