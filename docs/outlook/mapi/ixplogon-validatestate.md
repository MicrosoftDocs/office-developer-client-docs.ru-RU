---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439487"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет внешнее состояние поставщика транспорта. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением проверки состояния и результатами проверки состояния. Можно установить следующие флаги:
    
ABORT_XP_HEADER_OPERATION 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. Поставщик транспорта может продолжить работу над операцией или отменить операцию и вернуть MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Проверяет состояние загруженных поставщиков транспорта, вызывая метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) пулом MAPI. Этот флаг также предоставляет пулу MAPI возможность исправить критические сбои поставщика транспорта без принудительного отключения клиентских приложений и повторного входа в систему. 
    
FORCE_XP_CONNECT 
  
> Пользователь выбрал операцию подключения. Если этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие подключения происходит без кэшинга.
    
FORCE_XP_DISCONNECT 
  
> Пользователь выбрал операцию отключения. Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие отключения происходит без кэшинга.
    
PROCESS_XP_HEADER_CACHE 
  
> Записи в таблице кэша загона должны быть обработаны, все сообщения, помеченные флагом MSGSTATUS_REMOTE_DOWNLOAD, должны быть загружены, а все сообщения с флагом MSGSTATUS_REMOTE_DELETE должны быть удалены. Сообщения, для MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE, должны быть перемещены.
    
REFRESH_XP_HEADER_CACHE 
  
> Необходимо скачать новый список заглавных сообщений, а также очистить все флаги пометки состояния сообщения.
    
SUPPRESS_UI 
  
> Не позволяет поставщику транспорта отображать пользовательский интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция; его следует разрешить завершить или остановить перед попыткой выполнения этой операции.
    
MAPI_E_NO_SUPPORT 
  
> Задействованный удаленный поставщик транспорта не поддерживает пользовательский интерфейс, а в самом клиенте должно отобразиться диалоговое окно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::ValidateState** для поддержки вызовов метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния. Поставщик транспорта должен отвечать на вызов **IXPLogon::ValidateState** точно так же, как если бы пулер MAPI открыл объект состояния для текущего сеанса и затем вызвал **IMAPIStatus::ValidateState** для этого объекта. 
  
Чтобы поддерживать реализацию **IMAPIStatus::ValidateState,** пулер MAPI вызывает **IXPLogon::ValidateState** для всех объектов для запуска всех активных поставщиков транспорта, работающих в сеансе профиля. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

