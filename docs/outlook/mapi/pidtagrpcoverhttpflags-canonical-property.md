---
title: Каноническое свойство PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388268"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Каноническое свойство PidTagRpcOverHttpFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит параметры профиля, используемые Microsoft Office Outlook для подключения к Microsoft Exchange Server с помощью удаленный вызов процедур (RPC) по протоколу (HTTP).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROH_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6623  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Свойство **PR_ROH_FLAGS** хранится в разделе глобальные профиля в профиль по программированию интерфейса MAPI (Messaging Application). Значение **PR_ROH_FLAGS** является битовой маской, состоящий из одного или нескольких из следующих флагов. 
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Подключитесь к серверу Exchange, используя протокол RPC over HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Подключитесь к серверу Exchange, только с помощью Secure сокетов протокол SSL.  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Взаимная проверка подлинности сеанса при подключении с помощью протокола SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |В быстрых сетях: подключение по протоколу HTTP. Подключитесь с помощью протокола TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |В медленных сетях: подключение по протоколу HTTP. Подключитесь с помощью протокола TCP/IP.  <br/> |
   
Например, установка **PR_ROH_FLAGS** свойство, чтобы включить RPC через HTTP, протокол SSL, а также указать, следует сначала использовать протокол HTTP при медленном подключении задайте значение свойства **PR_ROH_FLAGS** для `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` которого равен 0x23. 
  
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

