---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 34c15ca4f7d81eeeee71fb0cb7e31085c75e5492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809455"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Относится к**: Outlook 
  
Удаляет регистрацию объекта для уведомление об изменениях хранилища сообщений, ранее созданные с помощью вызова метода [IMSLogon::Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Число подключений к регистрации, возвращаемых вызовом **IMSLogon::Advise**.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Сообщение метода **IMSLogon::Unadvise** для освобождения указатель на объект приемника уведомлений, переданной в параметре _lpAdviseSink_ в предыдущем вызове **IMSLogon::Advise**, тем самым Отмена уведомление внедряемые поставщиками хранилищ Регистрация. Как часть пропуск указатель на объект приемника уведомлений вызывается метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) объекта. Как правило, называется **выпуска** во время вызова **Unadvise** . Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
