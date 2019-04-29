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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439445"
---
# <a name="pidlidremotetransport-canonical-property"></a>Каноническое свойство PidLidRemoteTransport

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет учетную запись, с которой связан элемент заголовка, в первую очередь для реализации функции POP на сервере. 
  
|||
|:-----|:-----|
|Связанные свойства  <br/> |Диспидремотексп  <br/> |
|Набор свойств:  <br/> |Псетид_ремоте  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008F03  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Удаленное сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство относится только к сообщениям, у которых есть класс сообщения IPM. Удаленного. В Microsoft Outlook поддерживается сопоставление различных учетных записей, которые загружаются в заданное хранилище в сообщении со сведениями о папке (ФАИ), но эти сведения также могут храниться в реестре.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]] 
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

