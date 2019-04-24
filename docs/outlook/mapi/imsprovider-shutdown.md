---
title: Имспровидершутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317264"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ЗаКрывает поставщик хранилища сообщений в определенном порядке.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _Лпулфлагс_
  
> возврата Резервирования должен быть нулевым указателем.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **функцииimsprovider:: Shutdown** непосредственно перед освобождением объекта поставщика хранилища сообщений. MAPI освобождает все объекты входа для поставщика до **завершения** вызова для этого поставщика. 
  
## <a name="see-also"></a>См. также



[IMSProvider : IUnknown](imsprovideriunknown.md)

