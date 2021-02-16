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
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435903"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает объект состояния поставщика транспорта.
  
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
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта транспортного логотипа. Передача NULL возвращает [интерфейс IMAPIStatus.](imapistatusimapiprop.md) Параметр  _lpInterface_ также может быть задан в качестве идентификатора интерфейса для объекта. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта состояния. Можно установить следующий флаг:
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. Интерфейс по умолчанию является только для чтения. 
    
 _lpulObjType_
  
> [out] Указатель на тип открытого объекта.
    
 _lppEntry_
  
> [out] Указатель на указатель на открытый объект состояния.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::OpenStatusEntry,** когда клиентский приложение вызывает метод **OpenEntry** для идентификатора записи в строке таблицы состояния поставщика транспорта. **OpenStatusEntry** открывает объект с интерфейсом **IMAPIStatus,** связанным с этим конкретным поставщиком транспорта. Этот объект затем используется для того, чтобы клиентские приложения могли вызывать методы **IMAPIStatus** (например, для перенастройки сеанса logon с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или для проверки состояния сеанса logon с помощью метода [IMAPIStatus::ValidateState).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

