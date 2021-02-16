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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устанавливает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет настройкой хранения сообщений по умолчанию. Эти флаги являются взаимоисключающими; Можно установить только один из следующих флагов:
    
MAPI_DEFAULT_STORE
  
> Устанавливает хранилище сообщений в качестве сеанса по умолчанию. Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
MAPI_PRIMARY_STORE
  
> Устанавливает хранилище сообщений как хранилище, которое будет использоваться при logon. Если хранилище сообщений не является хранилищем по умолчанию, клиенты должны сделать его хранилищем по умолчанию. Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_PRIMARY_STORE в столбце **PR_RESOURCE_FLAGS** сообщений. 
    
MAPI_SECONDARY_STORE
  
> Устанавливает хранилище сообщений как хранилище, которое будет использоваться при logon, если основное хранилище сообщений не доступно. Если клиенту не удается открыть основное хранилище, он должен открыть дополнительное хранилище и установить его по умолчанию. Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_SECONDARY_STORE в столбце **PR_RESOURCE_FLAGS** сообщений. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS хранения сообщений в строке **таблицы состояния,** строке таблицы для хранения сообщений и профиле сеанса. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS хранения сообщений в строке **таблицы состояния** и строке таблицы для хранения сообщений. Профиль не изменен. 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи в хранилище сообщений, который предназначен по умолчанию. Если клиент передает значение NULL в  _lpEntryID,_ хранилище сообщений не выбрано по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::SetDefaultStore** создает хранилище сообщений как одно из следующих: 
  
- Хранилище сообщений по умолчанию для сеанса.
    
- Основное хранилище сообщений для сеанса.
    
- Дополнительное хранилище сообщений для сеанса.
    
Чтобы установить хранилище сообщений по умолчанию, в свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)должны быть установлены следующие флаги:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы определить хранилище сообщений по умолчанию для сеанса, необходимо получить таблицу состояния и найти параметр флага STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS.** Строка с этим параметром представляет хранилище сообщений, назначенное по умолчанию сеансом. 
  
Если установлен MAPI_DEFAULT_STORE или MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет профиль, таблицу хранения сообщений и таблицу состояния. 
  
При изменении параметра по умолчанию для хранения сообщений создаются следующие уведомления:
  
- Уведомление **о событии fnevTableModified** выдано для каждой затронутой строки как в хранилище сообщений, так и в таблице состояния. 
    
- Для пула MAPI выдано внутреннее уведомление. Операции, которые уже находятся в процессе выполнения, завершались без изменений; новые операции, которые включают хранилище сообщений по умолчанию, например загрузку сообщений, обрабатываются для нового магазина по умолчанию.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI использует метод **IMAPISession::SetDefaultStore,** чтобы установить выбранное хранилище как хранилище по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

