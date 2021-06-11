---
title: Именованные свойства MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435049"
---
# <a name="mapi-named-properties"></a>Именованные свойства MAPI
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет средство для назначения имен свойствам, сопоставления этих имен с уникальными идентификаторами и для сохраняния этого сопоставления. Сохраняемое имя для сопоставления идентификаторов гарантирует, что имена свойств остаются действительными во всех сеансах.
  
Чтобы определить имя свойства, клиент или поставщик услуг составляет имя и хранит его в [структуре MAPINAMEID.](mapinameid.md) Так как имена состоит из 32-битного глобально уникального идентификатора или GUID, а также строки символов Unicode или числового значения, создатели именных свойств могут создавать значимые имена, не опасаясь дублирования. Имена уникальны, и их можно использовать без оценок их идентификаторов. 
  
Чтобы поддерживать названные свойства, поставщик служб реализует два метода : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — для перевода между именами и идентификаторами и для того, чтобы разрешить его методам [IMAPIProp:GetProps](imapiprop-getprops.md)[IMAPIProp:SetProps](imapiprop-setprops.md) для получения и изменения свойств с помощью идентификаторов в диапазоне именных свойств. Диапазон именных идентификаторов свойств находится между 0x8000 и 0xFFFE. 
  
Любой объект, реализуя **интерфейс IMAPIProp,** может поддерживать названные свойства. Поставщики адресных книг, которые позволяют копировать записи других поставщиков в контейнеры и поставщики магазинов сообщений, которые могут использоваться для создания произвольных типов сообщений, необходимы для обеспечения этой поддержки. Это вариант для всех других поставщиков услуг. Поставщики, которые не поддерживают именимые свойства, возвращают MAPI_E_NO_SUPPORT из методов **GetIDsFromNames** и **GetNamesFromIDs** и отказываются устанавливать свойства с идентификаторами 0x8000 или больше, возвращая MAPI_E_UNEXPECTED в **SPropProblemarray**.
  
Создание имен для свойств — это один из способов для клиентов определить новые свойства для существующих или настраиваемых классов сообщений. Поставщики услуг могут использовать свойства с именами для разоблачения уникальных функций своих систем обмена сообщениями. Еще одним использованием именных свойств является предоставление альтернативного способа ссылок на свойства с идентификаторами ниже 0x8000. 
  
Например, клиент может использовать код, аналогичный следующему коду, чтобы получить имена для всех свойств объекта с именем:
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

Чтобы запросить все имена из набора свойств PS_PUBLIC_STRINGS, клиент заменит NULL в параметре набора свойств на PS_PUBLIC_STRINGS следующим образом: 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)

