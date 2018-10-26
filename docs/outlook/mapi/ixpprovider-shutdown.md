---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592607"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Закрывает вниз поставщика транспорта определенным образом.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно завершает работу поставщика транспорта.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPProvider::Shutdown** перед освобождение объекта поставщика транспорта. Прежде чем вызывать **Завершение работы**MAPI освобождает все объекты входа в систему для поставщика.
  
## <a name="see-also"></a>См. также



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

