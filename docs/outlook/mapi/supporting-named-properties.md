---
title: Поддержка именных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434328"
---
# <a name="supporting-named-properties"></a>Поддержка именных свойств

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Поддержка именных свойств требуется для: 
  
- Поставщики адресных книг, которые позволяют копировать записи других поставщиков в контейнеры.
    
- Поставщики хранения сообщений, которые можно использовать для создания произвольных типов сообщений.
    
Поддержка имени свойств необязательна для всех других поставщиков услуг. Поставщики служб, которые поддерживают названные свойства, должны реализовать сопоставление имен и идентификаторов в [методах IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Клиенты звонят **в GetNamesFromID,** чтобы получить соответствующие имена для одного или более идентификаторов свойств в диапазоне более 0x8000 и **GetIDsFromNames** для создания или получения идентификаторов для одного или более имен. 
  
Поставщики услуг, которые не поддерживают названные свойства, должны:
  
- Сбой вызовов [в IMAPIProp::SetProps](imapiprop-setprops.md) для набора свойств с идентификаторами 0x8000 или больше, возвращая MAPI_E_UNEXPECTED_ID в [массиве SPropProblem.](spropproblem.md) 
    
- Возврат MAPI_E_NO_SUPPORT из [методов IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

