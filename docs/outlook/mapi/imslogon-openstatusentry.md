---
title: IMSLogonOpenStatusEntry
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
  
Открывает объект состояния.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для открываемого объекта состояния. Передача NULL означает, что возвращается стандартный интерфейс для объекта (в данном случае интерфейс [IMAPIStatus).](imapistatusimapiprop.md) Параметр  _lpInterface_ также может быть задан в качестве идентификатора для соответствующего интерфейса объекта. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта состояния. Можно установить следующий флаг:
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты создаются с разрешением только на чтение, и клиентские приложения не должны работать при предположении, что разрешение на чтение и записи было предоставлено. 
    
 _lpulObjType_
  
> [out] Указатель на тип открытого объекта.
    
 _lppEntry_
  
> [out] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики store сообщений реализуют метод **IMSLogon::OpenStatusEntry** для открытия объекта состояния. Этот объект состояния затем используется для того, чтобы клиенты могли вызывать методы [IMAPIStatus.](imapistatusimapiprop.md) Например, клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для перенастройки сеанса работы с хранилищем сообщений или метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса для сеанса для работы с хранилищем сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

