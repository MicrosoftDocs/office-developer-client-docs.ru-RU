---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Получает имя профиля учетной записи.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807845"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Получает имя профиля учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parameters

_pwszIdentity_
  
> [in] [out] Имя профиля.
    
_pcch_
  
> [in] [out] При вызове этого метода, содержит размер (в символах) _pwszIdentity_ , которая была распределена. При возврате содержит длину, включая символ, заканчивающийся 0, от имени возвращенные профилей. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_OUTOFMEMORY  <br/> |Имя возвращаемых профиля превышает размер _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ имеет значение NULL.  <br/> |
   
## <a name="remarks"></a>Замечания

Если _pwszIdentity_ слишком мал для хранения имени профиля, не будет установлен при возвращении и _pcch_ будет указывать размера для _pwszIdentity_.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

