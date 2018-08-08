---
title: Каноническое свойство PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810524"
---
# <a name="pidlidremotetransport-canonical-property"></a>Каноническое свойство PidLidRemoteTransport

  
  
**Относится к**: Outlook 
  
Определяет, какая учетная запись элемент заголовка связан с, в основном для реализации оставлять POP на функциональность сервера. 
  
|||
|:-----|:-----|
|Связанными свойствами  <br/> |dispidRemoteXP  <br/> |
|Набор свойств:  <br/> |PSETID_Remote  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008F03  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Удаленные сообщения  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является релевантным только на сообщения, для которых классом сообщений IPM. Удаленный. Microsoft Outlook сохраняет сопоставление различные учетные записи, которые загружаются для заданного хранилища в сообщении связанные сведения о папке (FAI), но она может синхронизировать эту информацию в реестре.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

