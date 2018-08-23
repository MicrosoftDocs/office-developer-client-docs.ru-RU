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
ms.openlocfilehash: 72a26875802b2b7f94261f11e78fe560e9cc49d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583430"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMsgStore::Advise](imsgstore-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, связанный с регистрацию active уведомлений. Необходимо, значение _ulConnection_ возвращена предыдущий вызов метода **IMsgStore::Advise** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::Unadvise** отменяет регистрацию для уведомлений. Выпуски **Unadvise** указатель вызывающего абонента уведомить приемника, полученных в вызове **уведомлений** , используемые для регистрации. 
  
Как правило **Unadvise** вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) приемник уведомлений во время вызова **Unadvise** . Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

