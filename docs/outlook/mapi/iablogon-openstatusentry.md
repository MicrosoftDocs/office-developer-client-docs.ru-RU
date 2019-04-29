---
title: Иаблогонопенстатусентри
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
  
Открывает объект Status поставщика.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Параметры

 _Лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который должен использоваться для доступа к объекту Status. При передаче значения NULL возвращается стандартный интерфейс объекта [имапистатус: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют способом открытия объекта Status. Можно задать следующий флаг:
    
МАПИ_МОДИФИ 
  
> ЗаПрашивает разрешение на чтение и запись. По умолчанию объекты открываются с доступом только для чтения, а абоненты не должны предполагать, что предоставлено разрешение на чтение и запись.
    
 _Лпулобжтипе_
  
> вышли Указатель на тип открытого объекта.
    
 _Лппентри_
  
> вышли Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и открыт объект Status.
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют метод **опенстатусентри** , чтобы предоставить доступ к объекту своего состояния. Все поставщики адресных книг необходимы для реализации объекта status, который поддерживает, по крайней мере, метод [имапистатус:: валидатестате](imapistatus-validatestate.md) . Дополнительные сведения: [Реализация объекта Status](status-object-implementation.md).
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

