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
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335768"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает числовые маркеры, которые метод [IMAPISession::ShowForm](imapisession-showform.md) использует для доступа к сообщению. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к сообщению. Передача **null** приводит к стандартному интерфейсу или [используемой IMessage.](imessageimapiprop.md) Параметр _lpInterface должен_ быть null или **IID_IMessage.** 
    
 _lpMessage_
  
> [in] Указатель на сообщение, отображаемую в форме.
    
 _lpulMessageToken_
  
> [вышел] Указатель на маркер сообщения, который используется методом **IMAPISession::ShowForm** для доступа к сообщению, на которое указывает _lpMessage._
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Подготовка формы прошла успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::P repareForm** создает маркер сообщения для сообщения, на который указывает параметр _lpMessage,_ и вызывает метод [IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) Этот маркер передается в _параметре ulMessageToken_ **в IMAPISession::ShowForm.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вызов **PrepareForm** удался, отпустите сообщение, на которое указывает _lpMessage,_ позвонив по его методу [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) перед вызовом **ShowForm.** Невыполнение сообщения перед вызовом **ShowForm** может привести к утечке памяти. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI использует метод **IMAPISession::P repareForm,** а также **IMAPISession::ShowForm** для отображения сообщения в модальной форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

