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
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432123"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует службу сообщений в профиль. 
  
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
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор службы сообщений для копирования. 
    
 _lpszDisplayName_
  
> [in] Этот параметр является неподготовленным. 
    
 _lpInterfaceToCopy_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к разделу профиля службы сообщений для копирования. Передача NULL приводит к стандартному интерфейсу раздела профиля [IProfSect,](iprofsectimapiprop.md)который используется.
    
 _lpInterfaceDst_
  
> [in] Указатель на IID, который представляет интерфейс, используемый для доступа к объекту, на который указывает параметр _lpObjectDst._ Передача NULL приводит к использования интерфейса [сеанса IMAPISession.](imapisessioniunknown.md) Для  _параметра lpInterfaceDst_ также можно установить IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Указатель на указатель на объект администрирования сеанса или службы сообщений. Тип объекта должен соответствовать идентификатору интерфейса, переданного _в lpInterfaceDst._ Допустимые указатели объектов — LPMAPISESSION и LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows this method displays.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет копированием службы сообщений. Можно установить следующие флаги:
    
SERVICE_UI_ALWAYS 
  
> Запрашивает, чтобы служба сообщений всегда отображала таблицу свойств конфигурации.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений успешно скопирована.
    
MAPI_E_NO_ACCESS 
  
> Служба сообщений уже находится в профиле и не разрешает несколько экземпляров.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID, на** который указывает _lpUID,_ не относится к существующей службе сообщений. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::CopyMsgService** копирует службу сообщений в профиль, активный профиль или другой профиль. Профиль, содержащий службу сообщений для копирования и назначения, не должен быть тем же профилем, но может быть. 
  
Функция точки входа службы сообщений не вызвана для операции копирования. Скопированная служба сообщений имеет те же параметры конфигурации, что и исходный. Чтобы изменить эти параметры, клиент должен вызвать метод [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

