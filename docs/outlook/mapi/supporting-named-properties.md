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
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434328"
---
# <a name="supporting-named-properties"></a>Поддержка именованных свойств

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Поддержка именованных свойств необходима для следующих компонентов: 
  
- Поставщики адресных книг, которые позволяют копировать записи из других поставщиков в свои контейнеры.
    
- Поставщики хранилищ сообщений, которые можно использовать для создания произвольных типов сообщений.
    
Поддержка именованных свойств является необязательной для всех остальных поставщиков услуг. Поставщики услуг, которые поддерживают именованные свойства, должны реализовать сопоставление имен и идентификаторов в методах [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) и [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) . Клиенты вызывают **жетнамесфромидс** , чтобы получить соответствующие имена для одного или нескольких идентификаторов свойств в диапазоне от 0x8000 и **жетидсфромнамес** , чтобы создать или получить идентификаторы для одного или нескольких имен. 
  
Поставщики услуг, не поддерживающие именованные свойства, должны:
  
- Вызовы Fail для [IMAPIProp:: SetProps](imapiprop-setprops.md) для задания свойств с идентификаторами 0x8000 и выше, возвращая мапи_е_унекспектед_ид в массиве [спроппроблем](spropproblem.md) . 
    
- Возвращает МАПИ_Е_НО_СУППОРТ из методов [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) и [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) . 
    

