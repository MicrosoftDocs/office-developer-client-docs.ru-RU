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
ms.openlocfilehash: 165fe3a72060e88dc34d8153c13ae58bcbd9ae0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809660"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Относится к**: Outlook 
  
Проверяет состояние внешних поставщика транспорта. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяет, как выполняется проверка состояния и результатов Проверка состояния. Можно задать следующие флажки:
    
ABORT_XP_HEADER_OPERATION 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. Поставщика транспорта имеет параметр, чтобы продолжить работу над операции или может прервать операцию и вернуть MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Проверяет состояние поставщиков в настоящее время загрузки транспорта, вызывающие диспетчер очереди MAPI для вызова метода их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Этот флаг также предоставляет диспетчер очереди MAPI для исправления ошибок критические поставщика транспорта без перезагрузки клиентских приложений, чтобы выйти и снова войти в систему. 
    
FORCE_XP_CONNECT 
  
> Пользователь выбрал операции подключения. Когда этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие подключения происходит без кэширования.
    
FORCE_XP_DISCONNECT 
  
> Пользователь выбрал операцию отключения. Когда этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действия отключения происходит без кэширования.
    
PROCESS_XP_HEADER_CACHE 
  
> Будут обрабатываться записей в таблице кэша заголовок, необходимо загрузить все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DOWNLOAD и все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DELETE подлежащий удалению. Необходимо переместить сообщения, для которых MSGSTATUS_REMOTE_DOWNLOAD и задать MSGSTATUS_REMOTE_DELETE.
    
REFRESH_XP_HEADER_CACHE 
  
> Необходимо загрузить новый список заголовки сообщений, а все состояния сообщения Пометка флаги должна быть удалена.
    
SUPPRESS_UI 
  
> Запрещает отображение пользовательского интерфейса поставщика транспорта.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
MAPI_E_BUSY 
  
> Другой операции находится в стадии разработки; должны для выполнения или должна быть остановлена перед выполняется эта операция.
    
MAPI_E_NO_SUPPORT 
  
> Используемые поставщик удаленного транспорта не поддерживает пользовательский интерфейс и само приложение клиента должны отображать диалоговое окно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::ValidateState** для поддержки вызовы метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния. Поставщика транспорта должны ответить на звонок **IXPLogon::ValidateState** точно так же, если диспетчер очереди MAPI открыт объект состояния для текущего сеанса и затем вызвать **IMAPIStatus::ValidateState** для этого объекта. 
  
Для поддержки его реализация **IMAPIStatus::ValidateState**, диспетчер очереди MAPI вызывает **IXPLogon::ValidateState** для всех объектов входа для всех поставщиков активный перенос, на которых выполняется в рамках сеанса профилей. 
  
## <a name="see-also"></a>См. также



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

