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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327449"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Каноническое свойство PidTagRpcOverHttpFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит параметры в профиле, используемом Microsoft Office Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC) над протоколом передачи Hypertext (HTTP).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROH_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6623  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Свойство **PR_ROH_FLAGS** хранится в разделе Глобальный профиль интерфейса программирования приложений для обмена сообщениями (MAPI). Значение PR_ROH_FLAGS **—** битмаска, которая состоит из одного или более из следующих флагов. 
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Подключение на Exchange Server С ПОМОЩЬЮ RPC над HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Подключение для Exchange Server только с помощью безопасного слоя socket (SSL).  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Взаимно проверка подлинности сеанса при подключении с помощью SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |В быстрых сетях сначала подключайтесь с помощью HTTP. Затем подключите с помощью TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |В медленных сетях сначала подключайтесь с помощью HTTP. Затем подключите с помощью TCP/IP.  <br/> |
   
Например, чтобы задать свойство **PR_ROH_FLAGS** включить RPC над HTTP, потребовать SSL и указать, что протокол HTTP следует использовать сначала при медленных подключениях, установите значение свойства **PR_ROH_FLAGS,** равное  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` 0x23. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

