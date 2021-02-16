---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410786"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает объект состояния поставщика.
  
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
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который должен использоваться для доступа к объекту состояния. Передача NULL возвращает стандартный интерфейс [объекта, IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта состояния. Можно установить следующий флаг:
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты открываются с доступом только для чтения, и вызывающим не следует предполагать, что разрешение на чтение и записи предоставлено.
    
 _lpulObjType_
  
> [out] Указатель на тип открытого объекта.
    
 _lppEntry_
  
> [out] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным, и был открыт объект status.
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют метод **OpenStatusEntry,** чтобы предоставить доступ к их объекту состояния. Все поставщики адресных книг необходимы для реализации объекта состояния, который поддерживает как минимум метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Дополнительные сведения см. в [реализации объекта status.](status-object-implementation.md)
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

