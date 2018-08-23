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
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571201"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса) объект состояния, чтобы открыть. Значение NULL указывает, что возвращаются стандартный интерфейс для объекта (в данном случае интерфейс [IMAPIStatus](imapistatusimapiprop.md) ). Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для объекта. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта состояния. Можно задать следующий флаг:
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты создаются с разрешением только для чтения и клиентские приложения не должны работать предполагается, что что назначено разрешение чтения и записи. 
    
 _lpulObjType_
  
> [out] Указатель на тип объекта открыт.
    
 _lppEntry_
  
> [out] Указатель на указатель на объект открыт.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики хранилища сообщений реализуйте метод **IMSLogon::OpenStatusEntry** открыть объект состояния. Этот объект состояния затем используется для предоставления клиентам для вызова метода [IMAPIStatus](imapistatusimapiprop.md) . Например клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для изменения конфигурации сеанса входа в систему хранения сообщений либо метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса входа в систему хранения сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

