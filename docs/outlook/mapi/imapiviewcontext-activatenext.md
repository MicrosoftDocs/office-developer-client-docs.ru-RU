---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588505"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Область применения**: Outlook 2013 | Outlook 2016 
  
Активирует следующий или предыдущий сообщения в том порядке, представление. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

_ulDir_
  
> [in] Предоставление сведений о сообщении активируется флаги состояния. Допустимый флаг следующие значения.
    
  - VCDIR_CATEGORY: Средство просмотра должно быть активировано сообщения в другой категории представления. — Это сообщение, чтобы активировать: 
        
    - Первое сообщение в категории, если этот флаг **или**ed с VCDIR_NEXT следующего представления. 
        
    - Последние сообщения в предыдущей категории представления, если этот флаг ed **или**с VCDIR_PREV и предыдущих категории развернут. 
        
    - Первое сообщение в предыдущем категории и предыдущей категории представления, если этот флаг ed **или**с VCDIR_PREV еще не развернут. В этом случае предыдущей категории проходит автоматического развертывания. 
        
  - VCDIR_DELETE: Средство просмотра должно быть активировано следующий или предыдущий сообщения текущего сообщения были удалены. 
        
  - VCDIR_MOVE: Средство просмотра должно быть активировано следующий или предыдущий сообщение так, как была перемещена текущего сообщения. 
        
  - VCDIR_NEXT: Средство просмотра должно быть активировано следующее сообщение в порядке представления. 
        
  - VCDIR_PREV: Средство просмотра должно быть активировано предыдущее сообщение в том порядке, представление. 
        
  - VCDIR_UNREAD: Средство просмотра должно быть активировано следующий или предыдущий непрочитанные сообщения в том порядке, представление. 
    
_prcPosRect_
  
> [in] Указатель на Windows **Прямоугольник** структура, содержащая размер и положение окна, которые будут использоваться для отображения активированные сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно активирована. 
    
S_FALSE 
  
> Сообщение успешно активирована, но другого типа формы был открыт в процессе.
    
## <a name="remarks"></a>Замечания

Объекты формы вызвать метод **IMAPIViewContext::ActivateNext** для изменения какие сообщения, отображаемого для пользователя. Значение, переданное в параметре _ulDir_ указывает, какие сообщения следует был активирован и, в некоторых случаях, почему. Флаги VCDIR_NEXT и VCDIR_PREVIOUS соответствуют пользователям, выбрав команду **следующий** или **Предыдущий** в представлении, соответственно. Эти операции обычно соответствуют Перемещение вверх или вниз одного сообщения в форме просмотра списка сообщений. 
  
VCDIR_DELETE VCDIR_MOVE установлены флаги и методами [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) и [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) соответственно. Реализации этих методов вызовите **ActivateNext** с соответствующие направление и затем выполнить запрошенную операцию в окне сообщения, если выполнены **ActivateNext** звонок. Средства просмотра формы обычно позволяют пользователям указать направление для перемещения в списке сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Реализация [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) предоставляет следующий или предыдущий сообщение в папке, в зависимости от _ulDir_, текущего сообщения. После возврата **ActivateNext** , вызовите [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) для получения указателя на вновь активированных сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **ActivateNext** возвращает S_FALSE или текущего сообщения не указан, процедура вашей стандартного завершения работы которого следует включить вызов метода [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) формы. Если отображается следующий или предыдущий сообщение, используйте окно прямоугольника, переданной в параметре _prcPosRect_ для его отображения. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |Mfcmapi (en) реализован метод **IMAPIViewContext::ActivateNext** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

