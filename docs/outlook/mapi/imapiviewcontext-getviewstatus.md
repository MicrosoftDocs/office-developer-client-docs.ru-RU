---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429020"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает текущее состояние просмотра. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [вышел] Указатель на битмаску флагов, обеспечивающих состояние зрителя. Можно установить следующие флаги:
    
VCSTATUS_CATEGORY 
  
> Существует следующее или предыдущее сообщение в другой категории. 
    
VCSTATUS_DELETE 
  
> Форма позволяет удалять сообщения. 
    
VCSTATUS_INTERACTIVE 
  
> В форме должен отображаться пользовательский интерфейс. Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на глагол, который обычно вызывает отображение пользовательского интерфейса. 
    
VCSTATUS_MODAL 
  
> Форма является модальной для зрителя. 
    
VCSTATUS_NEXT 
  
> В представлении есть следующее сообщение. 
    
VCSTATUS_PREV 
  
> В представлении имеется предыдущее сообщение. 
    
VCSTATUS_READONLY 
  
> Сообщение должно быть открыто в режиме только для чтения. Операции удаления, отправки и перемещения должны быть отключены. 
    
VCSTATUS_UNREAD 
  
> В представлении имеется следующее или предыдущее непрочитанные сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние зрителя было успешно возвращено.
    
## <a name="remarks"></a>Примечания

Объекты формы называют метод **IMAPIViewContext::GetViewStatus,** чтобы определить, активируется ли больше сообщений в представлении формы в обоих или обоих направлениях, в том  направлении, в котором команда **Next** активирует сообщения, в том направлении, в котором предыдущая команда активирует сообщения, или в обоих направлениях. Значение, на которые указывает параметр _lpulStatus,_ используется для определения допустимости флагов VCSTATUS_NEXT и VCSTATUS_PREV [для IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md) Если флаг VCSTATUS_DELETE, но не флаг VCSTATUS_READONLY, сообщение можно удалить с помощью метода [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md) 
  
Как правило, формы отключать команды меню и кнопки, если они не допустимы для контекста просмотра. Зритель может предупредить форму об изменении состояния, назвав метод [IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md) 
  
Флаг VCSTATUS_MODAL, если форма должна быть модальной в окне, ручка которого передается в более ранний вызов [IMAPIForm::D oVerb.](imapiform-doverb.md) Если VCSTATUS_MODAL, форма может использовать поток, на котором был выполнен вызов **DoVerb** до закрытия формы. Если VCSTATUS_MODAL не заданной, форма не должна быть модальной для этого окна и не должна использовать поток. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI реализует метод **IMAPIViewContext::GetViewStatus** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

