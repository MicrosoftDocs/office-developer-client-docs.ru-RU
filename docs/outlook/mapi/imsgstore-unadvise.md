---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309725"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет отправку уведомлений, ранее установленных с помощью вызова в [метод IMsgStore::Advise.](imsgstore-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер подключения, связанный с активной регистрацией уведомлений. Значение _ulConnection_ должно быть возвращено предыдущим вызовом в **метод IMsgStore::Advise.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация была успешно отменена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::Unadvise** отменяет регистрацию для уведомления. **Unadvise** выпускает указатель на раковину рекомендации вызываемой, которую он получил в вызове **Advise,** используемом для регистрации. 
  
Как правило, **Unadvise** вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) в процессе вызова **Unadvise.** Однако если другой поток вызывает метод [IMAPIAdviseSink::OnNotify,](imapiadvisesink-onnotify.md) вызов выпуска откладывается до возвращения метода **OnNotify.**  
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

