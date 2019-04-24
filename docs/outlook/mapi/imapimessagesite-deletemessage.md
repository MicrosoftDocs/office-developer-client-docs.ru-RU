---
title: Имапимессажеситеделетемессаже
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

## <a name="parameters"></a>Параметры

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

Объект Form вызывает метод **имапимессажесите::D елетемессаже** , чтобы удалить сообщение, отображаемое в данный момент в форме. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После возврата **DeleteMessage**объекты формы должны проверять новое сообщение, а затем отменять себя, если они не существуют. Чтобы определить, было ли сообщение **DeleteMessage** Message on Deleted или перемещено в папку " **Удаленные** ", объект формы может вызвать метод [имапимессажесите:: жетситестатус](imapimessagesite-getsitestatus.md) , чтобы определить, был ли возвращен флаг делете_ис_мове. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если реализация метода **DeleteMessage** в средстве просмотра формы перемещается к следующему сообщению после удаления сообщения, реализация должна вызвать метод [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) и перед выполнением операции ПЕРЕдается флаг вкдир_делете фактическое удаление. Если при реализации **DeleteMessage** в средстве просмотра формы перемещается удаленное сообщение (например, в папку " **Удаленные** "), реализация должна сохранять изменения в сообщении, если сообщение было изменено. 
  
Типичная реализация **DeleteMessage** выполняет следующие задачи: 
  
1. Если реализация перемещает сообщение, оно вызывает метод [иперсистмессаже:: Save](ipersistmessage-save.md) , передавая **значение NULL** в параметре _пмессаже_ , и **значение true** в параметре _фсамеаслоад_ . 
    
2. Он вызывает метод **имапивиевконтекст:: активатенекст** , передавая флаг вкдир_делете в параметр _улдир_ . 
    
3. Если произойдет сбой вызова **активатенекст** , возвращается значение. Если **активатенекст** возвращает S_FALSE, вызывается метод [Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) . 
    
4. Он удаляет или перемещает сообщение.
    
Чтобы получить структуру **Rect** , используемую окном формы, вызовите функцию Windows [жетвиндоврект](https://msdn.microsoft.com/library/ms633519) . 
  
Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер::D Елетемессаже  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

