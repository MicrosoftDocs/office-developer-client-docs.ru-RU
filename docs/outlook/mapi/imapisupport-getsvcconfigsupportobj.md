---
title: Имаписуппортжетсвкконфигсуппортобж
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316560"
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

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лппсвксуппорт_
  
> вышли Указатель на указатель на новый объект поддержки службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект поддержки конфигурации успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **имаписуппорт:: жетсвкконфигсуппортобж** реализован для всех объектов поддержки. Поставщики услуг вызывают **жетсвкконфигсуппортобж** , чтобы создать объект поддержки конфигурации для передачи в функцию точки входа службы сообщений. 
  
Функция точки входа службы сообщений основана на прототипе [мсгсервицеентри](msgserviceentry.md) и вызывается методами интерфейса [имсгсервицеадмин](imsgserviceadminiunknown.md) . Функция точки входа службы сообщений позволяет службам сообщений настраивать себя или выполнять другие действия при изменении профиля. Функции точки входа службы сообщений могут поддерживать изменения конфигурации, отображая страницу свойств или массив значений свойства, переданный методу [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

