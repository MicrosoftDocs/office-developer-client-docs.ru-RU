---
title: ИсоЦиалпровидерсоЦиалнетворкгуид
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285514"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Значение свойства

Указатель на значение GUID, которое представляет уникальный идентификатор для социальной сети.
  
## <a name="remarks"></a>Замечания

GUID должен быть неизменяемым и не должен изменяться, даже если версия поставщика изменяется.
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

