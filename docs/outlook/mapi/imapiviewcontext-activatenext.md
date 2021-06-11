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
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410618"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Область применения**: Outlook 2013 | Outlook 2016 
  
Активирует следующее или предыдущее сообщение в порядке представления. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

_ulDir_
  
> [in] Флаги состояния, которые дают сведения об активированном сообщении. Допустимые параметры флага:
    
  - VCDIR_CATEGORY. Просмотр должен активировать сообщение в другой категории представления. Необходимо активировать сообщение: 
        
    - Первое сообщение в следующей категории представлений, если этот флаг **или** ed с VCDIR_NEXT. 
        
    - Последнее сообщение в предыдущей категории представлений, если этот флаг или VCDIR_PREV, а предыдущая категория расширена.  
        
    - Первое сообщение в предыдущей категории представлений, если этот флаг или VCDIR_PREV и предыдущая категория не расширена.  В этом случае предыдущая категория проходит автоматическое расширение. 
        
  - VCDIR_DELETE. Просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение удалено. 
        
  - VCDIR_MOVE. Просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение было перемещено. 
        
  - VCDIR_NEXT. Просмотр должен активировать следующее сообщение в порядке представления. 
        
  - VCDIR_PREV. Просмотр должен активировать предыдущее сообщение в порядке представления. 
        
  - VCDIR_UNREAD. В порядке представления зрителю следует активировать следующее или предыдущее непрочитанные сообщения. 
    
_prcPosRect_
  
> [in] Указатель на структуру Windows **reCT,** содержащую размер и положение окна, которое будет использоваться для отображения активированного сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение было активировано успешно. 
    
S_FALSE 
  
> Сообщение было активировано успешно, но в процессе был открыт другой тип формы.
    
## <a name="remarks"></a>Примечания

Объекты формы звонят **методу IMAPIViewContext::ActivateNext,** чтобы изменить отображаемую пользователю сообщение. Значение, переданное в  _параметре ulDir,_ указывает, какое сообщение следует активировать и, в некоторых случаях, почему. Флаги VCDIR_NEXT и VCDIR_PREVIOUS соответствуют пользователям, выбрав в представлении команду **Next** или **Previous** соответственно. Эти операции обычно соответствуют перемещению вверх или вниз одного сообщения в списке сообщений для просмотра форм. 
  
Флаги VCDIR_DELETE и VCDIR_MOVE установлены методами [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) и [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) соответственно. Реализация этих методов вызвать **ActivateNext** с соответствующим направлением, а затем выполнить запрашиваемую операцию на сообщении, если **вызов ActivateNext** не сбой. Как правило, зрители форм позволяют пользователям указывать направление перемещения в списке сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) делает следующее или предыдущее сообщение в папке в зависимости от значения  _ulDir_, текущего сообщения. После **возвращения ActivatNext** позвоните [в IMAPIMessageSite::GetMessage,](imapimessagesite-getmessage.md) чтобы получить указатель на вновь активированное сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **activateNext** возвращает S_FALSE или если текущего сообщения нет, выполните обычную процедуру остановки, которая должна включать вызов метода [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) вашей формы. Если отображается следующее или предыдущее сообщение, используйте прямоугольник окна, переданный в  _параметре prcPosRect,_ чтобы отобразить его. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI реализует метод **IMAPIViewContext::ActivateNext** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

