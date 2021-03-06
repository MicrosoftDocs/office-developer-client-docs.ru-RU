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
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411311"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает объект поддержки службы сообщений.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppSvcSupport_
  
> [вышел] Указатель на указатель на новый объект поддержки службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно создан объект поддержки конфигурации.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::GetSvcConfigSupportObj** реализован для всех объектов поддержки. Поставщики услуг звонят **в GetSvcConfigSupportObj,** чтобы создать объект поддержки конфигурации, чтобы передать функцию точки входа службы сообщений. 
  
Функция точки входа службы сообщений основана на прототипе [MSGSERVICEENTRY](msgserviceentry.md) и вызвана методами [интерфейса IMsgServiceAdmin.](imsgserviceadminiunknown.md) Функция точки входа службы сообщений позволяет службам сообщений настраивать себя или выполнять другие действия при смене профиля. Функции точки входа службы сообщений могут поддерживать изменения конфигурации путем отображения листа свойств или массива значений свойств, передаваемых методу [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

