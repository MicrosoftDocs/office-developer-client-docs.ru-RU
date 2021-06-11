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
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409694"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Упорядоченно закрывает поставщика транспорта.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызову удалось отключить поставщика транспорта.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IXPProvider::Shutdown** незадолго до выпуска объекта поставщика транспорта. Перед **вызовом shutdown** MAPI выпускает все объекты с логотипом для поставщика.
  
## <a name="see-also"></a>См. также



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

