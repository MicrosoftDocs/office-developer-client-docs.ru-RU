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
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809351"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Относится к**: Outlook 
  
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
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для администрирования. 
    
 _ulFlags_
  
> [in] Всегда имеет значение NULL. 
    
 _lppProviderAdmin_
  
> [out] Указатель на указатель на объект администрирования поставщика.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Объект администрирования поставщика успешно возвращен.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID** , на который указывает _lpUID_ не существует. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::AdminProviders** предоставляет доступ к объекту администрирования поставщика. Администрирование поставщика — это объект, который поддерживает интерфейс [IProviderAdmin](iprovideradminiunknown.md) и позволяет клиентам для выполнения следующих: 
  
- Добавьте поставщиков услуг службы сообщений.
    
- Удаление поставщиков услуг из службы сообщений.
    
- Откройте разделы профилей.
    
- Доступ к таблице поставщика службы сообщений.
    
Типы изменений, которые могут производится службы сообщений во время профиля зависят от службы сообщений. Большинство служб сообщения не поддерживают изменения, такие как добавление и удаление поставщиков во время профиля.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для получения **MAPIUID** структуры для службы сообщений на администрирование, получение столбца свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений. Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |Mfcmapi (en) использует метод **IMsgServiceAdmin::AdminProviders** для открытия объект администрирования поставщика службы.  <br/> |
   
## <a name="see-also"></a>См. также



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

