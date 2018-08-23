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
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579545"
---
# <a name="mapi-named-properties"></a>Именованные свойства MAPI
 
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет средства для назначения имен свойств, для сопоставления этих имен с уникальными идентификаторами и предъявления сохраняемого это сопоставление. Постоянное имя для сопоставления идентификатора гарантирует, что имена свойств остаются действительными между сеансами.
  
Определение именованного свойства клиента или поставщика делает название и сохраняет его в структуре [MAPINAMEID](mapinameid.md) . Поскольку имена состоят из 32-разрядная версия глобальный уникальный идентификатор, или идентификатор GUID и либо значение символа Юникода строковые или числовые, создателей именованных свойств можно создать понятные имена не копирования. Имена являются уникальными и они могут использоваться независимо от значения идентификаторов. 
  
Чтобы обеспечить поддержку именованных свойств, поставщик службы реализует два метода — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — для перевода между имена и идентификаторы и разрешить его [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) методы для получения и изменение свойств с идентификаторами в диапазоне именованное свойство. Значения идентификаторов именованного свойства — от 0x8000 до 0xFFFE. 
  
Любой объект, реализующий интерфейс **IMAPIProp** может поддерживать именованных свойств. Поставщиками адресных книг, поддерживающих записи от других поставщиков копируются в своих сообщений и контейнеры хранения поставщиков, которые могут использоваться для создания типов сообщений произвольных необходимы для предоставления этой поддержки. Он может использоваться для других поставщиков услуг. Поставщики, которые не поддерживают именованные свойства возврата MAPI_E_NO_SUPPORT из методов **GetIDsFromNames** и **GetNamesFromIDs** и не будет задайте свойства с идентификаторами 0x8000 или более высокой версии, возвращает ошибку MAPI_E_UNEXPECTED в ** SPropProblemarray**.
  
Создание имен для свойства является одним из способов для клиентов определить новые свойства для существующего или пользовательских классов сообщений. Поставщиков услуг можно использовать именованные свойства для предоставления уникальных функций их систем обмена сообщениями. Пока другой именованных свойств используется для предоставления альтернативного способа ссылок на свойства с идентификаторами ниже 0x8000. 
  
Например клиент может использовать код, похожий на следующий код для извлечения имен для всех именованных свойств объекта:
  
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

Чтобы запросить все имена PS_PUBLIC_STRINGS набор свойств, клиент заменить NULL в параметре set свойства PS_PUBLIC_STRINGS следующим образом: 
  
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

