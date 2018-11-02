---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587021"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает объект состояние поставщика транспорта.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса) для входа в систему объекта транспорта. Передача NULL возвращает интерфейс [IMAPIStatus](imapistatusimapiprop.md) . Параметр _lpInterface_ можно также назначается идентификатор интерфейс для объекта. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта состояния. Можно задать следующий флаг:
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. Интерфейс по умолчанию доступен только для чтения. 
    
 _lpulObjType_
  
> [out] Указатель на тип объекта открыт.
    
 _lppEntry_
  
> [out] Указатель на указатель на объект открыт состояние.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::OpenStatusEntry** , когда клиентское приложение вызывает метод **OpenEntry** идентификатор записи поставщика транспорта состояние строки в таблице. **OpenStatusEntry** открывает объект с помощью интерфейса **IMAPIStatus** , связанный с этой конкретной транспорта поставщика входа. Этот объект используется для включения клиентских приложений для вызова метода **IMAPIStatus** (например, чтобы снова настроить сеанса входа в систему с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , или для проверки состояния сеанса входа в систему с помощью [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) метод). 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

