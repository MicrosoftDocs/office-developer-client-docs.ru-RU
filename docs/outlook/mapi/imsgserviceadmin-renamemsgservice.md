---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809359"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Относится к**: Outlook 
  
Рекомендуется использовать. Назначает новое имя службы сообщений. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений переименовать. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpszDisplayName_
  
> [in] Указатель на новое имя для службы сообщений.
    
## <a name="return-value"></a>������������ ��������

MAPI_E_NO_SUPPORT 
  
> MAPI не поддерживает переименование этой службы сообщений. **RenameMsgService** всегда возвращает значение. 
    
## <a name="remarks"></a>Замечания

Чтобы назначить новое имя службы сообщений, клиенты следует использовать свойство **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) службы сообщений. Имена поставщиков услуг службы сообщений сохраняются в их свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

