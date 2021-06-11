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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает объект состояния.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для открытия объекта состояния. Передача NULL указывает, что возвращается стандартный интерфейс объекта (в данном случае интерфейс [IMAPIStatus).](imapistatusimapiprop.md) Параметр  _lpInterface_ также может быть задан идентификатору для соответствующего интерфейса объекта. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект состояния. Можно установить следующий флаг:
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты создаются с разрешения только для чтения, и клиентские приложения не должны работать на предположении, что разрешение на чтение и записи было предоставлено. 
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppEntry_
  
> [вышел] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики магазинов сообщений реализуют **метод IMSLogon::OpenStatusEntry** для открытия объекта состояния. Этот объект состояния затем используется для того, чтобы клиенты могли вызывать [методы IMAPIStatus.](imapistatusimapiprop.md) Например, клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для перенастройки сеанса логотипа магазина сообщений или метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса логотипа магазина сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

