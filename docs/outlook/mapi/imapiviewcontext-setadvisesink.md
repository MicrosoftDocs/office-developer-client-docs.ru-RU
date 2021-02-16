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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Управляет регистрацией формы для получения уведомлений об изменениях в средстве просмотра. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Параметры

 _pmvns_
  
> [in] Указатель на объект- или NULL-указатель формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация или отмена уведомления формы успешно зарегистрированы.
    
## <a name="remarks"></a>Примечания

Объекты форм вызовите метод **IMAPIViewContext::SetAdviseSink,** чтобы зарегистрироваться, чтобы узнать об изменениях в средстве просмотра форм, или отменить предварительную регистрацию. Если  _для pmvns_ установлено NULL, форма хочет отменить регистрацию. Когда  _pmvns указывает_ на допустимый общую форму, форма хочет зарегистрироваться для будущих уведомлений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если **SetAdviseSink** включает указатель на осязатель с уведомлением формы, оохраняйте ссылку на него, пока не будет выполнен другой вызов **SetAdviseSink** для отмены уведомления. Отправьте уведомление при изменении в вашем представлении и при загрузке нового сообщения. 
  
Дополнительные сведения см. в сведениях об [отправке и получении уведомлений о формах.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI реализует метод **IMAPIViewContext::SetAdviseSink** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

