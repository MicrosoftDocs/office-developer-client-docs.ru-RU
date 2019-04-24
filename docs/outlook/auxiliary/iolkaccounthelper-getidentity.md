---
title: Иолкаккаунселпержетидентити
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

Обратитесь к разделу [иолкаккаунселпер](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Параметры

_Пвсзидентити_
  
> возврата вышли Имя профиля.
    
_пкч_
  
> возврата вышли При вызове этого метода содержит размер (в знаках) выделенного _пвсзидентити_ . После возврата содержит фактическую длину имени возвращаемого профиля, включая 0 — завершающий символ. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_OUTOFMEMORY  <br/> |Имя возвращаемого профиля превышает размер _пвсзидентити_.  <br/> |
|E_INVALIDARG  <br/> | _пкч_ имеет значение null.  <br/> |
   
## <a name="remarks"></a>Замечания

Если _пвсзидентити_ слишком мал для хранения имени профиля, он не будет установлен для возврата, а _пкч_ будет указывать на размер, необходимый для _пвсзидентити_.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

