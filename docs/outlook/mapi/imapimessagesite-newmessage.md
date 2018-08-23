---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 133a2ae3896b9aaedb502cb77516040c53584882
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563739"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает новое сообщение.
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Параметры

 _fComposeInFolder_
  
> [in] Указывает, в папке, какие сообщения следует включать в себя. Если эта переменная имеет значение FALSE, параметр _pFolderFocus_ игнорируется и просмотра формы можно создать сообщение в любой папке. Если эта переменная имеет значение TRUE и передается в параметре _pFolderFocus_ , сообщение состоит в текущую папку. Если эта переменная имеет значение TRUE, НЕНУЛЕВОЕ значение передается в _pFolderFocus_сообщение состоит в папке, на который указывает _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Указатель на папку, где создается новое сообщение.
    
 _pPersistMessage_
  
> [in] Указатель на объект формы для новой формы.
    
 _ppMessage_
  
> [out] Указатель на указатель на новое сообщение.
    
 _ppMessageSite_
  
> [out] Указатель на указатель на объект сайта сообщения для нового сообщения.
    
 _ppViewContext_
  
> [out] Указатель на указатель на контекст представления, подходящую для передачи в новую форму с помощью нового сообщения. Если форма реализует контекст представления, NULL может быть передан в параметре _ppViewContext_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объекты формы вызовите метод **IMAPIMessageSite::NewMessage** для создания нового сообщения. Форма использует **NewMessage** для получения новых сообщений и связанные сообщения сайта с его представления. Затем можно изменить нового сообщения. 
  
Путем передачи НЕНУЛЕВОЕ значение с помощью параметра _ppViewContext_ может также получить контекст связанным представлением. В этом контексте представления можно использовать непосредственно или объединять, переданной в новое сообщение. Если требуется полная реализация, передайте _ppViewContext_NULL.
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::NewMessage** для создания нового сообщения, создайте новое средство просмотра формы и вызова **SetPersist** , чтобы задать для сообщения на форму просмотра. И, наконец он возвращает средство просмотра формы как сайт сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

