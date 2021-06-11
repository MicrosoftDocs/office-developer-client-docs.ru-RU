---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430002"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует текущее сообщение в папку.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parameters

 _pFolderDestination_
  
> [in] Указатель на папку, в которой должно быть скопировано сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается на этом сайте сообщений.
    
## <a name="remarks"></a>Примечания

Объекты формы называют **метод IMAPIMessageSite::CopyMessage,** чтобы скопировать текущее сообщение в новую папку. **CopyMessage** не меняет отображаемого в настоящее время сообщения пользователю, и интерфейс для вновь созданного сообщения не возвращается в форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Типичная реализация метода **CopyMessage** выполняет следующие задачи: 
  
1. Создает новое сообщение для копирования текущего сообщения.
    
2. Вызывает [метод IPersistMessage:::Save](ipersistmessage-save.md) с указателем на новое сообщение в _параметре pMessage_ и FALSE в _параметре fSameAsLoad._ 
    
3. Вызывает [метод IPersistMessage::SaveCompleted,](ipersistmessage-savecompleted.md) передавая NULL в _параметре pMessage._ 
    
4. Вызывает [метод IMAPIProp::SaveChanges в](imapiprop-savechanges.md) новом сообщении. 
    
Список интерфейсов, связанных с серверами форм, см. в перечне [интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

