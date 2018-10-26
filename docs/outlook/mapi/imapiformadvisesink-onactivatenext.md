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
ms.openlocfilehash: 7e8fb69e7d25420186d7269943c5d957311e813d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581758"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, является ли форма может обрабатывать класса сообщений для следующего сообщения для отображения.
  
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
  
> [in] Битовой маски флагов клиента или поставщика, скопированные из следующего сообщения для отображения, свойство **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), который предоставляет сведения о состоянии содержимого таблицы, что это сообщение будет включена в.
    
 _ulMessageFlags_
  
> [in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) следующего сообщения для отображения, который показывает текущее состояние сообщения.
    
 _ppPersistMessage_
  
> [out] Указатель на указатель на реализацию [IPersistMessage](ipersistmessageiunknown.md) для объекта формы, используются для новой формы, если требуется новая форма. Могут быть возвращены указатель на значение NULL, если текущий объект формы можно использовать для отображения и сохраните следующее сообщение. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно и формы можно обработать следующее сообщение.
    
S_FALSE 
  
> Форма не обрабатывает класса сообщений для следующего сообщения.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormAdviseSink::OnActivateNext** помогут определить, является ли он может отображать следующее сообщение в папке формы. Следующее сообщение может быть сообщение любого класса, но обычно это же класс или связанных с ними класса. Это делает процесс чтения несколько сообщений того же класса более эффективным, включив клиентских приложений для повторного использования объекты формы, когда это возможно. 
  
Большинство объектов формы будет использоваться класс сообщения, на который указывает параметр _lpszMessageClass_ для определения, является ли они могут обрабатывать следующее сообщение. Обычно формы может обрабатывать сообщения, которые принадлежат классам подкласс, в дополнение к сообщениям, которые относятся к классу по умолчанию которых является класс формы по умолчанию. Тем не менее формы можно использовать для определения без вопрос ли сообщение может обрабатывать, такие как состояние отправленные и неотправленные следующего сообщения других факторов. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Возвращает значение S_OK и NULL в параметре _ppPersistMessage_ , если форма может обрабатывать класс сообщения. Если форма можно создать новую форму, которая может обрабатывать сообщения, форма не может обработать, выполните следующие действия: 
  
1. Вызов фабрики класса формы для создания экземпляра объекта формы.
    
2. Сохраните этот экземпляр в содержимое параметра указатель _ppPersistMessage_ . 
    
3. Возвращает значение S_OK.
    
Средство просмотра формы будут загружать сообщения с помощью метода [IPersistMessage::Load](ipersistmessage-load.md) , к которой принадлежит объект, на который указывает _ppPersistMessage_.
  
Если ни форма, ни форму, можно создать может обрабатывать следующее сообщение, возвращает S_FALSE. Тем не менее как правило, формы должен не возвращаемое это значение, так как он вызывает снижению производительности в средстве просмотра формы.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |Mfcmapi (en) использует метод **IMAPIFormAdviseSink::OnActivateNext** для реализации метода [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

