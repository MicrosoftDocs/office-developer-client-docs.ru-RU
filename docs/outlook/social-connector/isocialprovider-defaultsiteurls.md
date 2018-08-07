---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Возвращает массив строк, которые задают URL-адресов сайта для поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812719"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Возвращает массив строк, которые задают URL-адресов сайта для поставщика Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Значение свойства

Указатель на структуру, которая указывает массив строк, представляющих URL-адресов сайта для поставщика OSC.
  
## <a name="remarks"></a>Замечания

Поставщик может поддерживать несколько URL-адресов сайта. OSC задает свойство [ISocialSession::SiteUrl](isocialsession-siteurl.md) для оповещения поставщика URL-адрес выбранного сайта. 
  
Первый элемент массива используется OSC как URL-адрес сайта по умолчанию. Поставщик может возвращать дополнительные элементы в массиве URL-адрес сайта, но OSC не использует их. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

