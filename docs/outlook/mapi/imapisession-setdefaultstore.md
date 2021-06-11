---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426109"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Немного флагов, которые контролируют параметр магазина сообщений по умолчанию. Эти флаги являются взаимоисключающими; можно установить только один из следующих флагов:
    
MAPI_DEFAULT_STORE
  
> Устанавливает хранилище сообщений как по умолчанию сеанса. Обновляет строку таблицы состояния магазина сообщений, установив флаг STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
MAPI_PRIMARY_STORE
  
> Устанавливает хранилище сообщений в качестве магазина, который будет использоваться в logon. Если хранилище сообщений не является хранилищем по умолчанию, клиенты должны сделать его по умолчанию. Обновляет строку таблицы состояния магазина сообщений, установив флаг STATUS_PRIMARY_STORE в **столбце PR_RESOURCE_FLAGS.** 
    
MAPI_SECONDARY_STORE
  
> Устанавливает хранилище сообщений в качестве магазина, который будет использоваться в logon, если основной магазин сообщений не доступен. Если клиент не может открыть основной магазин, он должен открыть вторичный магазин и установить его по умолчанию. Обновляет строку таблицы состояния магазина сообщений, установив флаг STATUS_SECONDARY_STORE в **столбце PR_RESOURCE_FLAGS.** 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS магазина **сообщений** в строке таблицы состояния, строке таблицы хранения сообщений и профиле сеанса. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS  в строке таблицы состояния и строке таблицы хранения сообщений. Профиль не изменен. 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа в хранилище сообщений, предназначенный по умолчанию. Если клиент передает NULL в  _lpEntryID,_ хранилище сообщений не выбрано по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::SetDefaultStore** создает хранилище сообщений в качестве одного из следующих: 
  
- Хранилище сообщений по умолчанию для сеанса.
    
- Основной хранилище сообщений для сеанса.
    
- Вторичный хранилище сообщений для сеанса.
    
Чтобы установить хранилище сообщений по умолчанию, хранилище сообщений должно иметь следующие флаги в свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask):](pidtagstoresupportmask-canonical-property.md)
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете определить хранилище сообщений по умолчанию для сеанса, чтобы получить таблицу состояния и  найти параметр флага STATUS_DEFAULT_STORE в столбце PR_RESOURCE_FLAGS. Строка с этим параметром представляет хранилище сообщений, назначенное по умолчанию сеанса. 
  
Когда установлен MAPI_DEFAULT_STORE или флаг MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет профиль, таблицу хранения сообщений и таблицу состояния. 
  
При изменении параметра по умолчанию в хранилище сообщений создаются следующие уведомления:
  
- Уведомление **о событии fnevTableModified** выдано для каждой затронутой строки как в хранилище сообщений, так и в таблице состояния. 
    
- Внутренний уведомления выдан spooler MAPI. Операции, которые уже завершены, завершались без изменений; Для нового магазина по умолчанию обрабатываются новые операции, в которые включается хранилище сообщений по умолчанию, например загрузка сообщений.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI использует **метод IMAPISession::SetDefaultStore** для настройки выбранного магазина в качестве магазина по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

