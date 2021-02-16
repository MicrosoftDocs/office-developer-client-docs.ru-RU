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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Активирует следующее или предыдущее сообщение в порядке просмотра. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Параметры

_ulDir_
  
> [in] Флаги состояния, которые дают сведения о сообщении, которое необходимо активировать. Допустимые параметры флага:
    
  - VCDIR_CATEGORY: просмотр должен активировать сообщение в другой категории представления. Сообщение, которое необходимо активировать: 
        
    - Первое сообщение в следующей категории представления, если этот флаг **или** помечен VCDIR_NEXT. 
        
    - Последнее сообщение в предыдущей категории представления, если этот флаг or **ed** с VCDIR_PREV и предыдущая категория была расширена. 
        
    - Первое сообщение в предыдущей категории представления, если этот флаг or **ed** с VCDIR_PREV и предыдущая категория не расширяется. В этом случае предыдущая категория проходит автоматическое расширение. 
        
  - VCDIR_DELETE: просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение было удалено. 
        
  - VCDIR_MOVE: просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение было перемещено. 
        
  - VCDIR_NEXT: просмотр должен активировать следующее сообщение в порядке просмотра. 
        
  - VCDIR_PREV: просмотр должен активировать предыдущее сообщение в порядке просмотра. 
        
  - VCDIR_UNREAD: просмотр должен активировать следующее или предыдущее непрочитанные сообщения в порядке просмотра. 
    
_prcPosRect_
  
> [in] Указатель на структуру **RECT** Windows, содержащую размер и положение окна, которое будет использоваться для отображения активированного сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно активировано. 
    
S_FALSE 
  
> Сообщение успешно активировано, но в процессе была открыта форма другого типа.
    
## <a name="remarks"></a>Примечания

Объекты форм вызывали метод **IMAPIViewContext::ActivateNext,** чтобы изменить сообщение, отображаемого пользователю. Значение, переданное в  _параметре ulDir,_ указывает, какое сообщение следует активировать, и, в некоторых случаях, почему. Флаги VCDIR_NEXT и VCDIR_PREVIOUS соответствуют пользователям, которые выбирают в  представлении команду **"Далее"** или "Предыдущая" соответственно. Эти операции обычно соответствуют перемещению вверх или вниз одного сообщения в списке сообщений для просмотра формы. 
  
Флаги VCDIR_DELETE и VCDIR_MOVE устанавливаются методами [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) и [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) соответственно. Реализации этих методов **вызывали ActivateNext** с соответствующим направлением, а затем выполняли запрашиваемую операцию с сообщением, если вызов **ActivateNext** не был неудачным. Как правило, с помощью просмотра форм пользователи могут указать направление перемещения в списке сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) создает следующее или предыдущее сообщение в папке в зависимости от значения  _ulDir_, текущего сообщения. После **возврата ActivateNext** вызовите [IMAPIMessageSite::GetMessage,](imapimessagesite-getmessage.md) чтобы получить указатель на недавно активированное сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **ActivateNext** возвращает S_FALSE или если текущего сообщения нет, выполните обычную процедуру завершения работы, которая должна включать вызов метода [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) формы. Если отображается следующее или предыдущее сообщение, используйте прямоугольник окна, переданный в  _параметре prcPosRect,_ чтобы отобразить его. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI реализует метод **IMAPIViewContext::ActivateNext** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

