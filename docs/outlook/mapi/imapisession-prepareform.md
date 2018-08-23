---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d4b62c4131ecc58db6957144321146625b43f7bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591025"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает числовое маркера, который использует метод [IMAPISession::ShowForm](imapisession-showform.md) для доступа к сообщению. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к сообщения. **Значение null,** результаты тестирования в стандартный интерфейс или [IMessage](imessageimapiprop.md)используется. Параметр _lpInterface_ должно быть **равно null** или IID_IMessage. 
    
 _lpMessage_
  
> [in] Указатель на сообщение, отображаемое в форме.
    
 _lpulMessageToken_
  
> [out] Указатель на маркер сообщения, который используется для доступа к сообщения с помощью метода **IMAPISession::ShowForm** , на который указывает _lpMessage_.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Подготовка формы выполнена успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::PrepareForm** создает маркер сообщения для сообщения, на который указывает параметр _lpMessage_ и вызывает метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) сообщение. Этот маркер передается в параметре _ulMessageToken_ **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При успешном вызове **PrepareForm** освобождение сообщения, на который указывает _lpMessage_ путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) до вызова метода **ShowForm**. Освобождение сообщения, прежде чем вызывать **ShowForm** можно привести утечки памяти. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |Mfcmapi (en) использует метод **IMAPISession::PrepareForm** , а также **IMAPISession::ShowForm**для отображения сообщения в модальную форму.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

