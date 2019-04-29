---
title: Имслогонопенстатусентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413180"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает объект Status.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Параметры

 _Лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID) для открытого объекта Status. ЗНАЧЕНИЕ NULL указывает на то, что стандартный интерфейс для объекта возвращается (в данном случае это интерфейс [имапистатус](imapistatusimapiprop.md) ). Для параметра _лпинтерфаце_ также можно задать идентификатор для соответствующего интерфейса для объекта. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют способом открытия объекта Status. Можно задать следующий флаг:
    
МАПИ_МОДИФИ 
  
> ЗаПрашивает разрешение на чтение и запись. По умолчанию объекты создаются с разрешением только для чтения, а клиентские приложения не должны работать в предположении, что предоставлено разрешение на чтение и запись. 
    
 _Лпулобжтипе_
  
> вышли Указатель на тип открытого объекта.
    
 _Лппентри_
  
> вышли Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики хранилища сообщений реализуют метод **имслогон:: опенстатусентри** для открытия объекта Status. Этот объект Status затем используется, чтобы позволить клиентам вызывать методы [имапистатус](imapistatusimapiprop.md) . Например, клиенты могут использовать метод [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) для повторной настройки сеанса входа в хранилище сообщений или метода [Имапистатус:: валидатестате](imapistatus-validatestate.md) для проверки состояния сеанса входа в хранилище сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

