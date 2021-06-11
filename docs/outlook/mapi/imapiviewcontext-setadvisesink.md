---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419396"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет регистрацией формы для получения уведомлений об изменениях в зрителье. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parameters

 _pmvns_
  
> [in] Указатель на форму советую объекту раковины или NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация или отмена уведомления о форме увенчались успехом.
    
## <a name="remarks"></a>Примечания

Объекты формы звонят по методу **IMAPIViewContext::SetAdviseSink,** чтобы зарегистрироваться, чтобы узнать об изменениях в виде просмотра или отменить предварительную регистрацию. Когда  _pmvns_ задают NULL, форма хочет отменить регистрацию. Когда  _pmvns указывает_ на допустимую форму, советую раковину, форма хочет зарегистрироваться для будущих уведомлений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Когда **SetAdviseSink** включает указатель на раковину формы, сохраняйте ссылку на нее, пока не будет сделан другой вызов **SetAdviseSink** для отмены уведомления. Отправьте уведомление о том, когда в вашем зрителье происходит изменение и когда вы загружаете новое сообщение. 
  
Дополнительные сведения см. в [рублях Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI реализует метод **IMAPIViewContext::SetAdviseSink** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

