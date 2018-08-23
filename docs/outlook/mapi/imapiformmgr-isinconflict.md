---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 329771bf79e30f07c9de0a311aa2a836ca507c38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580035"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет ли формы можно обработать собственный конфликтов сообщения. Сообщение находится в конфликт, если она была отредактирована одновременно с более одного пользователя. Это может произойти в сообщения в общих папках.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Параметры

 _ulMessageFlags_
  
> [in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщение, указывающее текущее состояние сообщения.
    
 _ulMessageStatus_
  
> [in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое предоставляет дополнительные сведения о состоянии сообщения.
    
 _szMessageClass_
  
> [in] Строка, имена класс сообщения сообщения.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержащую сообщение. Параметр _pFolderFocus_ может быть NULL, если такая папка не существует (например, если сообщение встроена в другое сообщение). 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Форма не обрабатывает собственный конфликтов сообщения.
    
S_FALSE 
  
> Форма обрабатывает собственный конфликтов сообщения или сообщения, для которого был передан сведения не конфликта.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormMgr::IsInConflict** для обнаружения ли определенной формы не обрабатывает собственный конфликтов сообщения. **IsInConflict** проверяет битовой маски в параметрах _ulMessageFlags_ и _ulMessageStatus_ на наличие конфликта флаг. Если значение флага конфликта, **IsInConflict** разрешает класс сообщения, переданной в параметре _szMessageClass_ и возвращает значение S_OK, если форма не обрабатывает собственный конфликтов. **IsInConflict** возвращает S_FALSE, если форма обрабатывает собственный конфликтов. 
  
Формы, которая не обрабатывает собственный конфликтов необходимо открыть с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может использовать существующий объект формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения обычно иметь дело с конфликтами при перемещения приложений из одного сообщения на следующий или предыдущий сообщения в папке. Если сообщение находится в конфликт, но сервер формы для этого сообщения можно обрабатывать конфликты, клиентское приложение должно выполнить его обычным код для отображения сообщения следующий или предыдущий. Если сервер формы не может обработать конфликтов, клиентское приложение следует перейти, как если бы он был знают о класса сообщений для сообщений следующий или предыдущий. 
  
## <a name="see-also"></a>См. также



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

