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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382374"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Перемещает текущего сообщения в папку.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

 _pFolderDestination_
  
> [in] Указатель на папку, где перемещать сообщения.
    
 _pViewContext_
  
> [in] Указатель на объект контекста представления.
    
 _prcPosRect_
  
> [in] Указатель на структуру [Прямоугольник](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) , содержащий положение и размер окна текущей формы. Далее форме, отображаемой также использует этот прямоугольник окна. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается на этом сайте сообщения.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIMessageSite::MoveMessage** для перемещения текущего сообщения в новую папку. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Реализация средства просмотра формы **MoveMessage** необходимо вызвать метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , передав флаг VCDIR_MOVE, прежде чем фактически перемещение сообщения в новую папку. Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) . 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возврата **MoveMessage**форм необходимо проверить для текущего сообщения и затем закрыть сами, если не существует. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Не реализован.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы формы MAPI](mapi-form-interfaces.md)

