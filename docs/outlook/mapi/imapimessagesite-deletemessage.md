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
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321415"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет текущее сообщение.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

 _pViewContext_
  
> [in] Указатель на объект контекста представления.
    
 _prcPosRect_
  
> [in] Указатель на структуру [RECT,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) которая содержит размер и положение окна текущей формы. Следующая отображаемая форма также использует этот прямоугольник окна. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается на этом сайте сообщений.
    
## <a name="remarks"></a>Примечания

Объект формы вызывает **метод IMAPIMessageSite::D eleteMessage,** чтобы удалить сообщение, которое отображается в настоящее время. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возвращения **DeleteMessage** объекты формы должны проверить новое сообщение, а затем отклоняться, если их нет. Чтобы определить, было ли удалено или перемещено сообщение **DeleteMessage** в папку "Удаленные элементы", объект формы может вызвать [метод IMAPIMessageSite::GetSiteStatus,](imapimessagesite-getsitestatus.md) чтобы определить, был ли возвращен флаг DELETE_IS_MOVE.  
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если реализация метода **DeleteMessage** для просмотра формы перемещается к следующему сообщению после удаления сообщения, реализация должна вызвать метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) и передать флаг VCDIR_DELETE перед выполнением фактического удаления. Если реализация удаленных сообщений  (например, папки удаленных элементов) для  просмотра формы, реализация должна сохранить изменения в сообщении, если сообщение было изменено. 
  
Типичная реализация **DeleteMessage** выполняет следующие задачи: 
  
1. Если реализация перемещает сообщение, он вызывает [метод IPersistMessage::Save,](ipersistmessage-save.md) передавая **null** в _параметре pMessage_ и true **в** _параметре fSameAsLoad._ 
    
2. Он вызывает **метод IMAPIViewContext::ActivateNext,** передав флаг VCDIR_DELETE в _параметре ulDir._ 
    
3. Если вызов **ActivateNext** не удается, он возвращается. Если **activateNext** возвращает S_FALSE, он вызывает [метод IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md) 
    
4. Он удаляет или перемещает сообщение.
    
Чтобы получить **структуру RECT,** используемую в окне формы, позвоните в Windows [GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

