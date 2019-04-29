---
title: Имсгсервицеадминренамемсгсервице
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
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422105"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устаревшие. Назначает новое имя службе сообщений. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Параметры

 _Лпуид_
  
> возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для переименования службы сообщений. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпсздисплайнаме_
  
> возврата Указатель на новое имя для службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

МАПИ_Е_НО_СУППОРТ 
  
> MAPI не поддерживает переименование этой службы сообщений. **Ренамемсгсервице** всегда возвращает это значение. 
    
## <a name="remarks"></a>Примечания

Чтобы назначить новое имя службе сообщений, клиенты должны использовать свойство **пр_сервице_наме** ([PidTagServiceName](pidtagservicename-canonical-property.md)) службы сообщений. Имена поставщиков служб в службе сообщений хранятся в своих свойствах **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

