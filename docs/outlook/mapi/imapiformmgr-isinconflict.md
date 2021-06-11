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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, может ли форма обрабатывать собственные конфликты сообщений. Сообщение находится в конфликте, если оно одновременно редактировался более чем одним пользователем. Это может произойти с сообщениями в общедоступных папках.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameters

 _ulMessageFlags_
  
> [in] Указатель на битмаску **флагов, скопированные** из свойства PR_MESSAGE_FLAGS [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения.
    
 _ulMessageStatus_
  
> [in] Битмаска флагов, определенных клиентом или **поставщика,** скопированная из свойства [PR_MSG_STATUS (PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которое предоставляет дополнительные сведения о состоянии сообщения.
    
 _szMessageClass_
  
> [in] Строка, которая называет класс сообщения сообщения.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержаную сообщение. Параметр  _pFolderFocus_ может быть NULL, если такой папки нет (например, если сообщение встроено в другое сообщение). 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма не обрабатывает собственные конфликты сообщений.
    
S_FALSE 
  
> Форма обрабатывает собственные конфликты сообщений, или сообщение, для которого была передана информация, не конфликтуется.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr::IsInConflict,** чтобы узнать, не обрабатывает ли определенная форма собственные конфликты сообщений. **IsInConflict** проверяет битмаски в  _параметрах ulMessageFlags_ и  _ulMessageStatus_ на наличие флага конфликта. Если задан флаг конфликта, **IsInConflict** устраняет класс сообщений, переданный в  _параметре szMessageClass,_ и возвращает его S_OK, если форма не обрабатывает собственные конфликты. **IsInConflict** возвращает S_FALSE, если форма обрабатывает собственные конфликты. 
  
Форма, которая не обрабатывает собственные конфликты, должна быть открыта с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может повторно использовать существующий объект формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения обычно должны иметь дело с конфликтами при переходе приложений из одного сообщения в следующее или предыдущее сообщение в папке. Если сообщение находится в конфликте, но сервер форм для этого сообщения может обрабатывать конфликты, клиентская заявка должна выполнить свой обычный код для отображения следующего или предыдущего сообщения. Если сервер формы не может обрабатывать конфликты, клиентская заявка должна продолжаться так, как будто оно не знало о классе сообщений следующего или предыдущего сообщения. 
  
## <a name="see-also"></a>См. также



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

