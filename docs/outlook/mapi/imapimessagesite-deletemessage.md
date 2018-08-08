---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808959"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Относится к**: Outlook 
  
Удаление текущего сообщения.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

 _pViewContext_
  
> [in] Указатель на объект контекста представления.
    
 _prcPosRect_
  
> [in] Указатель на структуру [Прямоугольник](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) , содержащий положение и размер окна текущей формы. Далее форме, отображаемой также использует этот прямоугольник окна. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается на этом сайте сообщения.
    
## <a name="remarks"></a>Замечания

Объект формы вызывает метод **IMAPIMessageSite::DeleteMessage** для удаления сообщения, в настоящее время отображения формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возврата **DeleteMessage**объекты формы необходимо проверить наличие новых сообщений и затем закрыть сами, если не существует. Чтобы определить, было ли сообщение, которое применяются **DeleteMessage** удаления или перемещения в папки " **Удаленные** ", объект формы может вызывать метод [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) , чтобы определить, был возвращен ли флаг DELETE_IS_MOVE. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если средство просмотра формы реализация метода **DeleteMessage** перемещается на следующее сообщение после удаляет сообщение, реализация должна вызовите метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) и передайте флаг VCDIR_DELETE перед выполнением Фактические удаления. Если реализация средства просмотра формы **DeleteMessage** перемещение удаленных сообщений (например, для папки " **Удаленные** "), реализации необходимо сохранить изменения к сообщению, если сообщение было изменено. 
  
Типичное использование **DeleteMessage** выполняет следующие задачи: 
  
1. Если реализация перемещается сообщение, он вызывает метод [IPersistMessage::Save](ipersistmessage-save.md) , передав **значение null,** с помощью параметра _pMessage_ и **значение true,** с помощью параметра _fSameAsLoad_ . 
    
2. Он вызывает метод **IMAPIViewContext::ActivateNext** , передав флаг VCDIR_DELETE с помощью параметра _ulDir_ . 
    
3. Если происходит сбой вызова **ActivateNext** , возвращается. Если **ActivateNext** возвращает S_FALSE, он вызывает метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Он удаляет или перемещает сообщение.
    
Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Не реализован.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

