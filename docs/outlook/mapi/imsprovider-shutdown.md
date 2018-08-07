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
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809429"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Относится к**: Outlook 
  
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

