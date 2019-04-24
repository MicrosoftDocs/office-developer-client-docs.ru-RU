---
title: Иксплогонопенстатусентри
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356030"
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

## <a name="parameters"></a>Параметры

 _Лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID) для объекта входа в систему. При передаче значения NULL возвращается интерфейс [имапистатус](imapistatusimapiprop.md) . Для параметра _лпинтерфаце_ также можно задать идентификатор для интерфейса для объекта. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют способом открытия объекта Status. Можно задать следующий флаг:
    
МАПИ_МОДИФИ 
  
> ЗаПрашивает разрешение на чтение и запись. Интерфейс по умолчанию доступен только для чтения. 
    
 _Лпулобжтипе_
  
> вышли Указатель на тип открытого объекта.
    
 _Лппентри_
  
> вышли Указатель на указатель на объект состояния Opened.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI вызывает метод **иксплогон:: опенстатусентри** , когда клиентское приложение вызывает метод **OpenEntry** для идентификатора записи в строке таблицы состояний поставщика транспорта. **Опенстатусентри** открывает объект с интерфейсом **имапистатус** , связанным с этим конкретным входным поставщиком транспорта. Затем этот объект используется, чтобы разрешить клиентским приложениям вызывать методы **имапистатус** (например, для перенастройки сеанса входа с помощью метода [Имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) или для проверки состояния сеанса входа с помощью [ Имапистатус:: метод Валидатестате](imapistatus-validatestate.md) ). 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

