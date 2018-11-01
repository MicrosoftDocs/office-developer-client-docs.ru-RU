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
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572258"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает текущее состояние просмотра. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Параметры

 _lpulStatus_
  
> [out] Указатель на битовой маски флагов, предоставляя состояние просмотра. Можно задать следующие флажки:
    
VCSTATUS_CATEGORY 
  
> Имеется следующий или предыдущий сообщение в другой категории. 
    
VCSTATUS_DELETE 
  
> Форма позволяет удалить сообщения. 
    
VCSTATUS_INTERACTIVE 
  
> Форма должна пользовательского интерфейса. Если этот флаг не установлен, форма следует отключать отображение даже в ответ на команду, которая обычно вызывает пользовательский интерфейс для отображения пользовательского интерфейса. 
    
VCSTATUS_MODAL 
  
> Форма является модальным для просмотра. 
    
VCSTATUS_NEXT 
  
> В представлении имеется следующее сообщение. 
    
VCSTATUS_PREV 
  
> Существует предыдущее сообщение в представлении. 
    
VCSTATUS_READONLY 
  
> Сообщение является открываются в режиме только для чтения. Удаление, отправка и переместите операции должны быть отключены. 
    
VCSTATUS_UNREAD 
  
> В представлении имеется следующий или предыдущий непрочитанные сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Средство просмотра состояния успешно возвращен.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIViewContext::GetViewStatus** , чтобы определить, есть ли дополнительные сообщения будут активироваться в представлении формы в одном или обоих направлениях то есть в направлении, в котором активируется команда **Далее** сообщения в направление, в котором **Предыдущая** команда активирует сообщения, или в обоих направлениях. Значение, указывает параметр _lpulStatus_ используется для определения допустимости флаги VCSTATUS_NEXT и VCSTATUS_PREV для [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Если флаг VCSTATUS_DELETE, set, но не флаг VCSTATUS_READONLY, а затем сообщения можно удалить с помощью метода [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) . 
  
Как правило форм отключить команды меню и кнопки, если они не являются действительными для контекста средство просмотра. Средство просмотра можно предупредить формы на изменение состояния путем вызова метода [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) . 
  
Флаг VCSTATUS_MODAL имеет значение, если форма должна быть модальное окно, дескриптор которого передается в более ранних [IMAPIForm::DoVerb](imapiform-doverb.md) вызова. Если значение VCSTATUS_MODAL, форму можно использовать поток, на котором был выполнен вызов **DoVerb** , пока эта форма закрывается. Если VCSTATUS_MODAL не установлен, форма не должна быть модальное окно и не должны использовать потока. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |Mfcmapi (en) реализован метод **IMAPIViewContext::GetViewStatus** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

