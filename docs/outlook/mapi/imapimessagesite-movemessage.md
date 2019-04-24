---
title: Имапимессажеситемовемессаже
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ПереМещает текущее сообщение в папку.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

 _Пфолдердестинатион_
  
> возврата Указатель на папку, в которую перемещается сообщение.
    
 _Пвиевконтекст_
  
> возврата Указатель на объект контекста представления.
    
 _Пркпосрект_
  
> возврата Указатель на структуру [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) , которая содержит размер и положение окна текущей формы. В следующей отображаемой форме также используется этот прямоугольник окна. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_НО_СУППОРТ 
  
> Эта операция не поддерживается этим сайтом сообщений.
    
## <a name="remarks"></a>Замечания

Объекты формы вызывают метод **имапимессажесите:: мовемессаже** для перемещения текущего сообщения в новую папку. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **Мовемессаже** в средстве просмотра формы должна вызвать метод [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) , передав флаг вкдир_мове, прежде чем переносить сообщение в новую папку. Чтобы получить структуру **Rect** , используемую окном формы, вызовите функцию Windows [жетвиндоврект](https://msdn.microsoft.com/library/ms633519) . 
  
Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возврата **мовемессаже**формы должны проверять текущее сообщение, а затем отменять себя, если они не существуют. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: Мовемессаже  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

