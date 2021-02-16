---
title: Поддержка именуемой свойства
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
# <a name="supporting-named-properties"></a>Поддержка именуемой свойства

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Поддержка именуемой свойства необходима для: 
  
- Поставщики адресных книг, которые позволяют скопировать записи от других поставщиков в свои контейнеры.
    
- Поставщики store сообщений, которые могут использоваться для создания произвольных типов сообщений.
    
Поддержка именуемого свойства не является обязательной для всех остальных поставщиков услуг. Поставщики служб, которые поддерживают именуемые свойства, должны реализовать сопоставление имен и идентификаторов в методах [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Клиенты вызывать **GetNamesFromIDs,** чтобы получить соответствующие имена для одного или более идентификаторов свойств в диапазоне 0x8000 и **GetIDsFromNames** для создания или извлечения идентификаторов для одного или более имен. 
  
Поставщики услуг, которые не поддерживают именуемые свойства, должны:
  
- Сбой вызовов [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить свойства с идентификаторами 0x8000 или более, возвращая MAPI_E_UNEXPECTED_ID в [массиве SPropProblem.](spropproblem.md) 
    
- Возвращает MAPI_E_NO_SUPPORT из методов [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
    

