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
ms.openlocfilehash: 5bf2ff74f6cda01608efd4b372aa4b03468c820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808958"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Относится к**: Outlook 
  
Копирует текущего сообщения в папку.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Параметры

 _pFolderDestination_
  
> [in] Указатель на папку, где Копировать сообщение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается на этом сайте сообщения.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIMessageSite::CopyMessage** для копирования текущего сообщения в новую папку. **CopyMessage** не изменяет сообщение, в настоящее время отображается для пользователя и интерфейс для только что созданный сообщения не возвращаются в форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Типичное использование метода **CopyMessage** выполняет следующие задачи: 
  
1. Создание сообщения для текущего сообщения для копирования.
    
2. Вызывает метод [IPersistMessage::Save](ipersistmessage-save.md) с указатель на новое сообщение в параметре _pMessage_ и значение FALSE в параметре _fSameAsLoad_ . 
    
3. Вызывает метод [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , передав NULL в параметре _pMessage_ . 
    
4. Вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) нового сообщения. 
    
Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Не реализован.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

