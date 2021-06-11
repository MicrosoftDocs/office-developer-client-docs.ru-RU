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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверка внешнего состояния поставщика транспорта. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, как выполняется проверка состояния и результаты проверки состояния. Можно установить следующие флаги:
    
ABORT_XP_HEADER_OPERATION 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. Поставщик транспорта может продолжить работу над операцией или прервать операцию и MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Проверяет состояние загруженных поставщиков транспорта, вызывая вызов spooler MAPI их [метода IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Этот флаг также предоставляет шпалеру MAPI возможность исправить критические сбои поставщика транспорта, не вынуждая клиентские приложения выйти из системы и снова войти в систему. 
    
FORCE_XP_CONNECT 
  
> Пользователь выбрал операцию подключения. Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE флагом, действие подключения происходит без кэшинга.
    
FORCE_XP_DISCONNECT 
  
> Пользователь выбрал операцию отключения. Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие отключения происходит без кэшинга.
    
PROCESS_XP_HEADER_CACHE 
  
> Записи в таблице кэша загона должны обрабатываться, все сообщения с флагом MSGSTATUS_REMOTE_DOWNLOAD должны быть загружены, а все сообщения, помеченные флагом MSGSTATUS_REMOTE_DELETE, должны быть удалены. Сообщения с набором MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE должны быть перемещены.
    
REFRESH_XP_HEADER_CACHE 
  
> Необходимо скачать новый список загона сообщений, а также очистить все флаги, помеченные состоянием сообщений.
    
SUPPRESS_UI 
  
> Не позволяет поставщику транспорта отображать пользовательский интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается другая операция; его следует разрешить завершить или остановить перед попыткой выполнения этой операции.
    
MAPI_E_NO_SUPPORT 
  
> Участвующий поставщик удаленного транспорта не поддерживает пользовательский интерфейс, а само клиентские приложения должны отображать диалоговое окно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IXPLogon::ValidateState** для поддержки вызовов для [метода IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния. Поставщик транспорта должен отвечать на вызов **IXPLogon::ValidateState** так же, как если бы шпалер MAPI открыл объект состояния для текущего сеанса логотипа, а затем вызвал **IMAPIStatus::ValidateState** на этом объекте. 
  
Чтобы поддержать реализацию **IMAPIStatus::ValidateState,** шпалер MAPI вызывает **IXPLogon::ValidateState** для всех объектов с логотипом для всех активных поставщиков транспорта, которые работают в сеансе профиля. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

