---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411766"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, может ли форма обрабатывать класс сообщений следующего отображаемого сообщения.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in] Указатель на класс сообщений следующего сообщения.
    
 _ulMessageStatus_
  
> [in] Битмаска флагов, определенных клиентом или **поставщика,** скопированная из свойства [PR_MSG_STATUS (PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)следующего сообщения, которое предоставляет сведения о состоянии таблицы содержимого, в которую включено сообщение.
    
 _ulMessageFlags_
  
> [in] Указатель на битмаску **флагов, скопированные** из свойства [PR_MESSAGE_FLAGS (PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)следующего сообщения, отображаемого, что указывает текущее состояние сообщения.
    
 _ppPersistMessage_
  
> [вышел] Указатель на указатель на реализацию [IPersistMessage](ipersistmessageiunknown.md) для объекта формы, используемой для новой формы, если требуется новая форма. Указатель на NULL можно вернуть, если текущий объект формы можно использовать для отображения и сохранения следующего сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление было успешным, и форма может обрабатывать следующее сообщение.
    
S_FALSE 
  
> Форма не обрабатывает класс сообщений следующего сообщения.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormAdviseSink::OnActivateNext,** чтобы помочь форме определить, может ли она отображать следующее сообщение в папке. Следующее сообщение может быть сообщением любого класса, но обычно оно относится к одному классу или связанному классу. Это делает процесс чтения нескольких сообщений одного класса более эффективным, позволяя клиентские приложения по возможности повторно использовать объекты формы. 
  
Большинство объектов формы будут использовать класс сообщений, на который указывает параметр  _lpszMessageClass,_ чтобы определить, могут ли они обрабатывать следующее сообщение. Обычно форма может обрабатывать сообщения, которые относятся к классам, класс которых по умолчанию является подклассом, в дополнение к сообщениям, которые относятся к классу по умолчанию. Однако форма может использовать другие факторы, чтобы без вопросов определить, можно ли обрабатывать сообщение, например, отправленное или неавентное состояние следующего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Возврат S_OK и NULL в  _параметре ppPersistMessage,_ если форма может обрабатывать класс сообщений. Если форма может создать новую форму, которая может обрабатывать сообщение, которое форма не может обрабатывать, выполните следующие действия: 
  
1. Вызов фабрики классов формы для создания экземпляра нового объекта формы.
    
2. Храните этот экземпляр в содержимом _параметра указателя ppPersistMessage._ 
    
3. Возвращение S_OK.
    
Зритель формы загружает сообщение с помощью метода [IPersistMessage::Load,](ipersistmessage-load.md) который принадлежит объекту, на который указывает _ppPersistMessage._
  
Если ни форма, ни форма, которую вы можете создать, не смогут обрабатывать следующее сообщение, S_FALSE. Однако, как правило, формы не должны возвращать это значение, так как это приводит к снижению производительности в области просмотра форм.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI использует **метод IMAPIFormAdviseSink::OnActivateNext** для реализации метода [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

