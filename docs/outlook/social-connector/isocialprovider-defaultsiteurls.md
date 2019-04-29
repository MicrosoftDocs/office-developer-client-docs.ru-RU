---
title: ИсоЦиалпровидердефаултситеурлс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Возвращает массив строк, указывающих URL-адреса сайта для поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413775"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Возвращает массив строк, указывающих URL-адреса сайта для поставщика Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Значение свойства

Указатель на структуру, задающую массив строк, которые представляют URL-адреса сайтов для поставщика OSC.
  
## <a name="remarks"></a>Примечания

Поставщик может поддерживать несколько URL-адресов сайта. OSC задает свойство [настроенный ISocialSession:: SiteUrl](isocialsession-siteurl.md) для информирования поставщика о ВЫБРАНном URL-адресе сайта. 
  
В качестве URL-адреса сайта по умолчанию OSC использует первый элемент массива. Поставщик может возвращать дополнительные элементы в массиве URL-адресов сайта, но OSC не использует их. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

