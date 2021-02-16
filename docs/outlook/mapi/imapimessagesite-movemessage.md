---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321367"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перемещает текущее сообщение в папку.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

 _pFolderDestination_
  
> [in] Указатель на папку, в которой перемещается сообщение.
    
 _pViewContext_
  
> [in] Указатель на объект контекста представления.
    
 _prcPosRect_
  
> [in] Указатель на структуру [RECT,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) которая содержит размер и положение окна текущей формы. Следующая отображаемая форма также использует этот прямоугольник окна. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Эта операция не поддерживается на этом сайте сообщений.
    
## <a name="remarks"></a>Примечания

Объекты форм вызывать метод **IMAPIMessageSite::MoveMessage** для перемещения текущего сообщения в новую папку. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **MoveMessage** в представлении формы должна вызвать метод [IMAPIViewContext::ActivateNext,](imapiviewcontext-activatenext.md) передав флаг VCDIR_MOVE перед фактическим перемещением сообщения в новую папку. Чтобы получить **структуру RECT,** используемую окном формы, вызовите функцию Windows [GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возврата **MoveMessage** формы должны проверить текущее сообщение и затем отклоняться, если нет. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

