---
title: IMSProviderShutdown
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
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589093"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Закрывает поставщика хранилища сообщений определенным образом.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in] Зарезервировано; должен быть указатель нулевое значение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **IMSProvider::Shutdown** перед объект поставщика хранилища сообщений. MAPI освобождает все объекты входа в систему для поставщика, прежде чем вызывать **Завершение работы** для этого поставщика. 
  
## <a name="see-also"></a>См. также



[IMSProvider : IUnknown](imsprovideriunknown.md)

