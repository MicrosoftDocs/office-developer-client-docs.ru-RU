---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422763"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений, которая должна администрироваться. 
    
 _ulFlags_
  
> [in] Всегда NULL. 
    
 _lppProviderAdmin_
  
> [out] Указатель на указатель на объект администрирования поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект администрирования поставщика успешно возвращен.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID, на** который указывает _lpUID,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::AdminProviders** предоставляет доступ к объекту администрирования поставщика. Администрирование поставщика — это объект, который поддерживает [интерфейс IProviderAdmin](iprovideradminiunknown.md) и позволяет клиентам: 
  
- Добавление поставщиков служб в службу сообщений.
    
- Удаление поставщиков услуг из службы сообщений.
    
- Откройте разделы профиля.
    
- Доступ к таблице поставщика службы сообщений.
    
Типы изменений, которые фактически можно внести в службу сообщений во время использования профиля, зависят от службы сообщений. Однако большинство служб сообщений не поддерживают такие изменения, как добавление и удаление поставщиков, пока используется профиль.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить структуру **MAPIUID** для службы сообщений для **администрирования,** извлекает столбец свойства PR_SERVICE_UID ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений. Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI использует метод **IMsgServiceAdmin::AdminProviders** для открытия объекта администрирования поставщика для службы.  <br/> |
   
## <a name="see-also"></a>См. также



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

