---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e5ccadbd6df664b6650487f340508ae4548a1c2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583269"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получение сведений о состоянии, связанные с сообщение в определенной папке (например, будет ли это сообщение помечено для удаления).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для сообщения, состояние которого получается.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulMessageStatus_
  
> [out] Указатель на указатель битовой маски флагов, которые указывают состояние сообщения. Цифры от 0 до 15 бит зарезервированы и должно быть равно нулю; бит 16 до 31 доступны для использования реализации. Можно задать следующие флажки:
    
MSGSTATUS_DELMARKED 
  
> Сообщение было помечено для удаления.
    
MSGSTATUS_HIDDEN 
  
> Сообщение является не будет отображаться. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Это сообщение будет отображаться выделенный.
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента.
    
MSGSTATUS_TAGGED 
  
> Сообщение уже помечен для определенного клиента цели.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние сообщения был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::GetMessageStatus** возвращает состояние сообщения. Состояние сообщения хранится в свойстве **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщение. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Как задать, снят и используется биты состояния сообщение полностью зависит от реализации, за исключением того, что бит 0 до 15 зарезервированы и должно быть равно нулю. При сохранении сообщения в поддерева IPM MAPI оставляет за собой биты 16 до 31 для использования клиентами IPM. Если хранение сообщений в другие поддеревьев, можно использовать бит 16 до 31 для внутреннего использования.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |Mfcmapi (en) использует метод **IMAPIFolder::GetMessageStatus** , чтобы получить сведения о состоянии следующее сообщение для отображения.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal и OpenMessageModal  <br/> |Mfcmapi (en) использует метод **IMAPIFolder::GetMessageStatus** , чтобы получить сведения о состоянии сообщение, отображаемое для передачи для просмотра формы, который является CMyMAPIFormViewer или [IMAPISession::ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

