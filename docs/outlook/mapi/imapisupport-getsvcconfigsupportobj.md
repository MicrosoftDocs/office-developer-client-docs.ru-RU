---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1c48ceefa84658b236b8dfa4e10df18c175d920e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595162"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает объект сообщения службы поддержки.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppSvcSupport_
  
> [out] Указатель на указатель на новый объект сообщения службы поддержки.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Объект поддержки конфигурации успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::GetSvcConfigSupportObj** применяется для всех объектов поддержки. Поставщики услуг вызова **GetSvcConfigSupportObj** для создания объекта поддержки конфигурации для передачи сообщений функции точки входа службы. 
  
Функция точки входа службы сообщений на основании прототип [MSGSERVICEENTRY](msgserviceentry.md) и вызывается методы интерфейса [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Функция точки входа службы сообщений позволяет службам сообщение настраиваться или другие действия при изменении профиля. Точка входа службы сообщений поддержку функций можно изменения конфигурации, отображая свойств или с помощью массива значение свойства, переданной в метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

