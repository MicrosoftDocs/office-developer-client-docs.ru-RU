---
title: Каноническое свойство PidTagRpcOverHttpProxyAuthScheme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea4b90bf1190fd71701f82d43aaee384c7987ed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387197"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>Каноническое свойство PidTagRpcOverHttpProxyAuthScheme

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет протокол проверки подлинности, которое будет использоваться для этого профиля.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|Идентификатор:  <br/> |0x6627  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство можно задать для обычной проверки подлинности или проверки подлинности NT LAN Manager (NTLM). Возможны следующие возможные значения для данного свойства.
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0x1  <br/> |Обычная проверка подлинности  <br/> |
|**ROHAUTH_NTLM** <br/> |0x2  <br/> |Проверка подлинности NTLM  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

