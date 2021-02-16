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
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438773"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указывает, в какой папке должно быть составлено сообщение. Если переменная имеет значение FALSE, параметр  _pFolderFocus_ игнорируется, и просмотр формы может создать сообщение в любой папке. Если переменная имеет значение TRUE и в параметре  _pFolderFocus_ передается значение NULL, сообщение будет составлено в текущей папке. Если переменная имеет значение TRUE и в _pFolderFocus_ передается значение, не состоящее из NULL, сообщение состоит из папки, на который указывает _pFolderFocus._
    
 _pFolderFocus_
  
> [in] Указатель на папку, в которой создается новое сообщение.
    
 _pPersistMessage_
  
> [in] Указатель на объект формы для новой формы.
    
 _ppMessage_
  
> [out] Указатель на указатель на новое сообщение.
    
 _ppMessageSite_
  
> [out] Указатель на указатель на объект сайта сообщения для нового сообщения.
    
 _ppViewContext_
  
> [out] Указатель на указатель на контекст представления, который подходит для передачи в новую форму с новым сообщением. Если форма реализует собственный контекст представления, в  _параметре ppViewContext_ можно передать NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объекты форм вызывать метод **IMAPIMessageSite::NewMessage** для создания нового сообщения. Форма использует **NewMessage** для получения нового сообщения и связанного сайта сообщений из своего представления. Затем оно может изменить новое сообщение. 
  
Вы также можете получить связанный контекст представления, передав в  _параметре ppViewContext_ значение, не связанное с NULL. Этот контекст представления можно использовать напрямую или агрегировать и передавать в новое сообщение. Если требуется полная реализация, передав NULL в _ppViewContext._
  
Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI использует метод **IMAPIMessageSite::NewMessage** для создания нового сообщения, создания нового представления формы и вызова **SetPersist,** чтобы настроить сообщение для просмотра формы. Наконец, оно возвращает просмотр формы в качестве сайта сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

