---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 791dfe094aa0ff1aab656b56fbdf7d59e880b92e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593734"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует службы сообщений в профиль. 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор службы сообщений для копирования. 
    
 _lpszDisplayName_
  
> [in] Этот параметр устарел. 
    
 _lpInterfaceToCopy_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля службы сообщений для копирования. Стандартный профиль раздел интерфейса, [IProfSect](iprofsectimapiprop.md)используется результаты передаче значения NULL.
    
 _lpInterfaceDst_
  
> [in] Указатель на ИД интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _lpObjectDst_ . В интерфейсе сеанса [IMAPISession](imapisessioniunknown.md)используется результаты передаче значения NULL. Параметр _lpInterfaceDst_ также может иметь значение IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Указатель на указатель на объект администрирования службы сеанса или сообщения. Тип объекта, должен соответствовать идентификатор интерфейса, переданные в _lpInterfaceDst_. Допустимый объект указатели — LPMAPISESSION и LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как скопировать службы сообщений. Можно задать следующие флажки:
    
SERVICE_UI_ALWAYS 
  
> Запросы на том, что служба сообщений всегда отображаются на листе свойств конфигурации.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений успешно скопирована.
    
MAPI_E_NO_ACCESS 
  
> Служба сообщений уже в профиле и не допускает несколько экземпляров.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID** , на который указывает _lpUID_ не относится к существующей службы сообщений. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::CopyMsgService** копирует службы сообщений в профиль текущей конфигурации или другого профиля. Профиль, который содержит службы сообщений для копирования и назначение не должны быть одного профиля, но они могут быть. 
  
Служба сообщений функции точки входа не вызывается для операции копирования. Служба скопированной сообщение имеет те же параметры конфигурации, что его исходный. Чтобы изменить эти параметры, клиент должен вызвать метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

