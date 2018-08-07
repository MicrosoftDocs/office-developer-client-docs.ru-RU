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
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808744"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Относится к**: Outlook 
  
Отменяет подключение к активного сеанса.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [In] Зарезервировано; должен быть указатель нулевое значение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Подключение успешно отменено.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

В реализации метода **завершения работы** выполните любые задачи вам необходимо учитывать необходимые. MAPI вызывает метод **Shutdown** только после выпустил всех объектов входа в систему. 
  
## <a name="see-also"></a>См. также



[IABProvider : IUnknown](iabprovideriunknown.md)

