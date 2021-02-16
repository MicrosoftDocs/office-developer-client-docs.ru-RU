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
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418640"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает состояние, связанное с сообщением в определенной папке (например, помечено ли это сообщение для удаления).
  
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
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для сообщения, состояние которого получено.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulMessageStatus_
  
> [out] Указатель на указатель на битовуюmask флагов, которые указывают на состояние сообщения. Биты от 0 до 15 зарезервированы и должны быть нулем; Биты от 16 до 31 доступны для реализации. Можно установить следующие флаги:
    
MSGSTATUS_DELMARKED 
  
> Сообщение помечено для удаления.
    
MSGSTATUS_HIDDEN 
  
> Сообщение не должно отображаться. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Сообщение должно быть выделено.
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки в локальный клиент.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение помечено для скачивания из удаленного хранения сообщений в локальный клиент.
    
MSGSTATUS_TAGGED 
  
> Сообщение помечено для определенной клиентом цели.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние сообщения было успешно извлечено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::GetMessageStatus** возвращает состояние сообщения. Состояние сообщения хранится в свойстве PR_MSG_STATUS **(** [PidTagMessageStatus).](pidtagmessagestatus-canonical-property.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Настройка, очистка и применение битов состояния сообщения полностью зависит от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны быть нулем. Если сообщения хранятся в подпотеке IPM, MAPI зарезервировать биты от 16 до 31 для использования клиентами IPM. Если сообщения хранятся в других подtrees, вы можете использовать биты от 16 до 31 для собственных целей.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI использует метод **IMAPIFolder::GetMessageStatus** для получения состояния следующего сообщения, которое будет отображаться.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal и OpenMessageModal  <br/> |MFCMAPI использует метод **IMAPIFolder::GetMessageStatus,** чтобы получить состояние сообщения, которое должно отображаться для передать в просмотр формы, который является CMyMAPIFormViewer или [IMAPISession::ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

