---
title: Копирование профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424730"
---
# <a name="copying-a-profile"></a>Копирование профиля

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Один из способов создания профиля — копирование из существующего профиля и изменение необходимых служб сообщений и поставщиков услуг. Копирование профиля включает в себя использование объекта администрирования профиля, предоставляемого MAPI с помощью функции [мапиадминпрофилес](mapiadminprofiles.md) . 
  
 **Копирование профиля**
  
1. ВыЗовите **мапиадминпрофилес** , чтобы получить указатель интерфейса **ипрофадмин** . 
    
2. Call [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Создайте ограничение свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем профиля, который необходимо скопировать. 
    
4. Call [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения соответствующей строки в таблице Profile. 
    
5. Call [ипрофадмин:: копипрофиле](iprofadmin-copyprofile.md), передавая значение столбца **пр_дисплай_наме** в качестве параметра _лпсзолдпрофиленаме_ . 
    

