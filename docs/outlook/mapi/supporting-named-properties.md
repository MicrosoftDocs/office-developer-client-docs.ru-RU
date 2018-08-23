---
title: Поддержка именованных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9ee41469914e52295af219428f26854662c9e2f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582248"
---
# <a name="supporting-named-properties"></a>Поддержка именованных свойств

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Поддержка именованных свойств является обязательным для: 
  
- Поставщиками адресных книг, которые позволяют записей от других поставщиков копируются в их контейнеров.
    
- Сообщение хранилища поставщиков, которые могут использоваться для создания типов произвольных сообщений.
    
Поддержка именованное свойство является необязательным для всех других поставщиков услуг. Поставщики услуг, которые поддерживают именованные свойства необходимо реализовать идентификатор имени сопоставления в методы [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Клиенты вызывать **GetNamesFromIDs** для извлечения соответствующих имен для одного или нескольких идентификаторов свойство в более чем диапазон 0x8000 и **GetIDsFromNames** для создания или получения идентификаторов для одно или несколько имен. 
  
Поставщики услуг, которые не поддерживают именованные свойства выполнить следующие действия:
  
- Не удается вызовы [IMAPIProp::SetProps](imapiprop-setprops.md) , чтобы задать свойства с идентификаторами 0x8000 или более высокой версии, возвращая MAPI_E_UNEXPECTED_ID в массиве [SPropProblem](spropproblem.md) . 
    
- Возвращает MAPI_E_NO_SUPPORT из методов [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

