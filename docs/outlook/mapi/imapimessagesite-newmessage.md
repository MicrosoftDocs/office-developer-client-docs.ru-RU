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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _fComposeInFolder_
  
> [in] Указывает, в какой папке должно быть составлено сообщение. Если переменная false, параметр  _pFolderFocus_ игнорируется, и зритель формы может составить сообщение в любой папке. Если переменная true и NULL передается в  _параметре pFolderFocus,_ сообщение состоит в текущей папке. Если переменная true и значение non-NULL передается в _pFolderFocus,_ сообщение состоит в папке, на которые указывает _pFolderFocus._
    
 _pFolderFocus_
  
> [in] Указатель на папку, в которой создается новое сообщение.
    
 _pPersistMessage_
  
> [in] Указатель на объект формы для новой формы.
    
 _ppMessage_
  
> [вышел] Указатель на указатель на новое сообщение.
    
 _ppMessageSite_
  
> [вышел] Указатель на указатель на объект сайта сообщений для нового сообщения.
    
 _ppViewContext_
  
> [вышел] Указатель на указатель контекста представления, который подходит для передачи в новую форму с новым сообщением. Если форма реализует собственный контекст представления, NULL можно передать в _параметре ppViewContext._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объекты форм называют **метод IMAPIMessageSite::NewMessage** для создания нового сообщения. Форма использует **NewMessage** для получения нового сообщения и связанного сайта сообщений из его представления. Затем он может изменить новое сообщение. 
  
Вы также можете получить связанный контекст представления, передав значение non-NULL в _параметре ppViewContext._ Этот контекст представления можно использовать непосредственно или агрегировать и передавать в новое сообщение. Если требуется полная реализация, передай NULL в _ppViewContext._
  
Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI использует **метод IMAPIMessageSite::NewMessage** для создания нового сообщения, мгновенного создания нового просмотра формы и вызова **SetPersist** для набора сообщения для просмотра формы. Наконец, он возвращает просмотр формы в виде сайта сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

