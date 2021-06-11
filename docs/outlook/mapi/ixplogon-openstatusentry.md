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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает объект состояния поставщика транспорта.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта транспортного логотипа. Передача NULL возвращает [интерфейс IMAPIStatus.](imapistatusimapiprop.md) Параметр  _lpInterface_ также может быть задан идентификатору интерфейса объекта. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект состояния. Можно установить следующий флаг:
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. Интерфейс по умолчанию только для чтения. 
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppEntry_
  
> [вышел] Указатель на указатель на открытый объект состояния.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает метод **IXPLogon::OpenStatusEntry,** когда клиентская заявка вызывает метод **OpenEntry** для идентификатора входа в строке таблицы состояния поставщика транспорта. **OpenStatusEntry** открывает объект с интерфейсом **IMAPIStatus,** связанным с этим логотипом поставщика транспорта. Этот объект затем используется для того, чтобы клиентские приложения могли вызывать методы **IMAPIStatus** (например, для перенастройки сеанса логотипа с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или проверки состояния сеанса логона с помощью метода [IMAPIStatus::ValidateState).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

