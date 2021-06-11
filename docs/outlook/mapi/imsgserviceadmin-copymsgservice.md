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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Указатель на [структуру MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор службы сообщений для копирования. 
    
 _lpszDisplayName_
  
> [in] Этот параметр был обесценив. 
    
 _lpInterfaceToCopy_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к разделу профилей службы сообщений для копирования. Передача NULL приводит к стандартному интерфейсу раздела профилей [IProfSect,](iprofsectimapiprop.md)который используется.
    
 _lpInterfaceDst_
  
> [in] Указатель на IID, который представляет интерфейс, используемый для доступа к объекту, на который указывает _параметр lpObjectDst._ Передача NULL приводит к интерфейсу [сеанса, используется IMAPISession.](imapisessioniunknown.md) Параметр  _lpInterfaceDst_ также может быть задан для IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Указатель на указатель на объект администрирования сеанса или службы сообщений. Тип объекта должен соответствовать идентификатору интерфейса, переданным _в lpInterfaceDst._ Допустимые указатели объектов LPMAPISESSION и LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.
    
 _ulFlags_
  
> [in] Битмаски флагов, которые контролируют копирование службы сообщений. Можно установить следующие флаги:
    
SERVICE_UI_ALWAYS 
  
> Запрашивает, чтобы служба сообщений всегда отображала лист свойств конфигурации.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений успешно скопирована.
    
MAPI_E_NO_ACCESS 
  
> Служба сообщений уже находится в профиле и не позволяет использовать несколько экземпляров.
    
MAPI_E_NOT_FOUND 
  
> **MapIUID,** на который указывает _lpUID,_ не относится к существующей службе сообщений. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::CopyMsgService** копирует службу сообщений в профиль, активный профиль или другой профиль. Профиль, содержащий скопированную службу сообщений и пункт назначения, не должен быть таким же профилем, но может быть. 
  
Функция точки входа службы сообщений не называется для операции копирования. Скопированная служба сообщений имеет те же параметры конфигурации, что и оригинал. Чтобы изменить эти параметры, клиент должен вызвать [метод IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

