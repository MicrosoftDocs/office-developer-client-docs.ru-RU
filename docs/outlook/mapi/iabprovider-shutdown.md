---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567890"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет подключение к активного сеанса.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [In] Зарезервировано; должен быть указатель нулевое значение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Подключение успешно отменено.
    
## <a name="notes-to-implementers"></a>Примечания для реализующих

В реализации метода **завершения работы** выполните любые задачи вам необходимо учитывать необходимые. MAPI вызывает метод **Shutdown** только после выпустил всех объектов входа в систему. 
  
## <a name="see-also"></a>См. также



[IABProvider : IUnknown](iabprovideriunknown.md)

