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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, может ли форма обрабатывать класс сообщения следующего сообщения для отображения.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Параметры

 _lpszMessageClass_
  
> [in] Указатель на класс сообщения следующего сообщения.
    
 _ulMessageStatus_
  
> [in] Битоваяmass клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)следующего сообщения, которое предоставляет сведения о состоянии таблицы содержимого, в которую включено сообщение.
    
 _ulMessageFlags_
  
> [in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)следующего сообщения, которое будет отображаться, которое указывает текущее состояние сообщения.
    
 _ppPersistMessage_
  
> [out] Указатель на указатель на реализацию [IPersistMessage](ipersistmessageiunknown.md) для объекта формы, используемой для новой формы, если требуется новая форма. Если текущий объект формы можно использовать для отображения и сохранения следующего сообщения, можно вернуть указатель на NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно, и форма может обработать следующее сообщение.
    
S_FALSE 
  
> Форма не обрабатывает класс сообщения следующего сообщения.
    
## <a name="remarks"></a>Примечания

С помощью метода **IMAPIFormAdviseSink::OnActivateNext** форма может определить, может ли форма отображать следующее сообщение в папке. Следующее сообщение может быть сообщением любого класса, но обычно оно относится к одному классу или связанному классу. Это делает процесс чтения нескольких сообщений одного класса более эффективным, позволяя клиентские приложения по возможности повторно использовать объекты форм. 
  
Большинство объектов форм будут использовать класс сообщения, на который указывает параметр  _lpszMessageClass,_ чтобы определить, могут ли они обрабатывать следующее сообщение. Обычно форма может обрабатывать сообщения, принадлежащие классам, класс формы по умолчанию которых является подклассом, в дополнение к сообщениям, принадлежащим к классу по умолчанию. Однако форма может использовать другие факторы, чтобы определить, можно ли обрабатывать сообщение, например, состояние "отправлено" или "не является" следующего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Возвращает S_OK и NULL в  _параметре ppPersistMessage,_ если форма может обрабатывать класс сообщения. Если форма может создать форму, которая может обрабатывать сообщение, которое не может обрабатывать форма, выполните следующие действия. 
  
1. Вызовите фабрику классов формы, чтобы создать экземпляр нового объекта формы.
    
2. Храните этот экземпляр в содержимом параметра _указателя ppPersistMessage._ 
    
3. Возврат S_OK.
    
Просмотр форм загрузит сообщение с помощью метода [IPersistMessage::Load,](ipersistmessage-load.md) который принадлежит объекту, на который указывает _ppPersistMessage._
  
Если ни форма, ни форма, которую вы можете создать, не могут обрабатывать следующее сообщение, S_FALSE. Однако в целом формы не должны возвращать это значение, так как это приводит к снижению производительности в представлении формы.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI использует метод **IMAPIFormAdviseSink::OnActivateNext** для реализации метода [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

