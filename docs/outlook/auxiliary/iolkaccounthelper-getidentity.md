---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Получает имя профиля учетной записи.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322108"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Получает имя профиля учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parameters

_pwszIdentity_
  
> [in] [вышел] Имя профиля.
    
_pcch_
  
> [in] [вышел] При вызове этого метода содержится размер (в количестве символов) _выделенного объекта pwszIdentity._ По возвращении содержит фактическую длину, включая символ 0-terminating, возвращенного имени профиля. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_OUTOFMEMORY  <br/> |Имя возвращенного профиля больше размера _pwszIdentity._  <br/> |
|E_INVALIDARG  <br/> | _pcch_ — это NULL.  <br/> |
   
## <a name="remarks"></a>Примечания

Если  _pwszIdentity_ слишком мал для удержания имени профиля, оно не будет задано по возвращении, и  _pcch_ будет указать размер, необходимый  _для pwszIdentity_.
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

