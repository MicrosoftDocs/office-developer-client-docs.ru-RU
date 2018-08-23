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
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583185"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Управляет формы регистрации для получения уведомлений об изменениях в средстве просмотра. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Параметры

 _pmvns_
  
> [in] Указатель на форме уведомить приемник object или значение NULL.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация или отмены для уведомления формы выполнено успешно.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIViewContext::SetAdviseSink** , чтобы зарегистрировать сведения об изменениях в форме просмотра или отменить предварительная регистрация. Когда _pmvns_ имеет значение NULL, форма, где требуется реализовать для отмены регистрации. При _pmvns_ указывает на допустимый формы уведомить приемник, формы требуется зарегистрировать для уведомления. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Когда **SetAdviseSink** включает в себя формы уведомить указателя приемника, продолжайте ссылки на нее до другого **SetAdviseSink** вызов Отмена уведомлений. Отправьте уведомление, когда происходит изменение в вашей средства просмотра и при загрузке нового сообщения. 
  
Для получения дополнительных сведений см [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |Mfcmapi (en) реализован метод **IMAPIViewContext::SetAdviseSink** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

