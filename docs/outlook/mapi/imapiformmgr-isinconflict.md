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
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412886"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет, может ли форма обрабатывать собственные конфликты сообщений. Сообщение конфликтует, если оно было одновременно изменено более чем одним пользователем. Это может произойти с сообщениями в общедоступных папках.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Параметры

 _ulMessageFlags_
  
> [in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения.
    
 _ulMessageStatus_
  
> [in] Битовая почта клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которая предоставляет дополнительные сведения о состоянии сообщения.
    
 _szMessageClass_
  
> [in] Строка, которая именует класс сообщения.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержаную сообщение. Параметр  _pFolderFocus_ может иметь NULL, если такая папка не существует (например, если сообщение внедрено в другое сообщение). 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма не обрабатывает собственные конфликты сообщений.
    
S_FALSE 
  
> Форма обрабатывает собственные конфликты сообщений или сообщение, сведения о котором были переданы, не конфликтуют.
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIFormMgr::IsInConflict,** чтобы определить, не обрабатывает ли конкретная форма собственные конфликты сообщений. **IsInConflict** проверяет битовыеmasks в  _параметрах ulMessageFlags_ и  _ulMessageStatus_ на наличие флага конфликта. Если установлен флаг конфликта, **IsInConflict** разрешает класс сообщения, переданный в  _параметре szMessageClass,_ и возвращает S_OK, если форма не обрабатывает собственные конфликты. **IsInConflict** возвращает S_FALSE, если форма обрабатывает собственные конфликты. 
  
Форма, не обрабатывающая собственные конфликты, должна быть открыта с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может повторно использовать существующий объект формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения обычно должны иметь дело с конфликтами, когда приложения перемещаются из одного сообщения в следующее или предыдущее сообщение в папке. Если сообщение конфликтует, но сервер форм для этого сообщения может обработать конфликты, клиентские приложения должны выполнить свой обычный код для отображения следующего или предыдущего сообщения. Если сервер форм не может обработать конфликты, клиентские приложения должны продолжать работу так, как если бы он не знал о классе сообщения следующего или предыдущего сообщения. 
  
## <a name="see-also"></a>См. также



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

