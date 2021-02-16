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
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI обеспечивает возможность назначения имен свойствам, сопоставления этих имен с уникальными идентификаторами и для сохраняемого сопоставления. Постоянное имя сопоставления идентификаторов гарантирует, что имена свойств остаются действительными во время сеансов.
  
Чтобы определить именовамое свойство, клиент или поставщик услуг составляет имя и сохраняет его в структуре [MAPINAMEID.](mapinameid.md) Поскольку имена состоит из 32-битного глобально уникального идентификатора или GUID, а также строки символов Юникод или числимого значения, создатели именуемого свойства могут создавать осмысленные имена, не боясь дублирования. Имена уникальны, и их можно использовать без использования значений идентификаторов. 
  
Для поддержки именуемого свойства поставщик службы реализует два метода: [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — для перевода между именами и идентификаторами и для того, чтобы разрешить методы [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) для извлечения и изменения свойств с идентификаторами в именоваемом диапазоне свойств. Диапазон идентификаторов именуемого свойства находится между 0x8000 и 0xFFFE. 
  
Любой объект, реализуя **интерфейс IMAPIProp,** может поддерживать именуемые свойства. Для данной поддержки требуются поставщики адресных книг, которые позволяют скопировать записи от других поставщиков в свои контейнеры и поставщики store сообщений, которые могут использоваться для создания произвольных типов сообщений. Это вариант для всех остальных поставщиков услуг. Поставщики, которые не поддерживают именуемые свойства, возвращают MAPI_E_NO_SUPPORT из методов **GetIDsFromNames** и **GetNamesFromIDs** и не устанавливают свойства с идентификаторами 0x8000 или больше, возвращая MAPI_E_UNEXPECTED в **SPropProblemarray.**
  
Создание имен для свойств — это один из способов определения клиентами новых свойств для существующих или настраиваемых классов сообщений. Поставщики услуг могут использовать именующие свойства для использования уникальных функций своих систем обмена сообщениями. Еще одно использование именуемого свойства — предоставление альтернативного способа ссылки на свойства с идентификаторами ниже 0x8000. 
  
Например, клиент может использовать код, подобный следующему, для получения имен всех именуемого свойства объекта:
  
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

Чтобы запросить все имена из PS_PUBLIC_STRINGS свойств, клиент заменит NULL в параметре набора свойств на PS_PUBLIC_STRINGS следующим образом: 
  
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

