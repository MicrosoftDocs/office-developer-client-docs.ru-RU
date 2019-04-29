---
title: Имапивиевконтекстсетадвисесинк
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

 _пмвнс_
  
> возврата Указатель на объект приемника уведомлений формы или значение NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление о регистрации или отмене для формы успешно завершено.
    
## <a name="remarks"></a>Примечания

Объекты форм вызовите метод **имапивиевконтекст:: сетадвисесинк** , чтобы узнать об изменениях в средстве просмотра форм или отменить предыдущую регистрацию. Если для _пмвнс_ ЗАДАНО значение null, форма хочет отменить регистрацию. Когда _пмвнс_ указывает на допустимый приемник рекомендаций формы, форма запрашивается для регистрации будущих уведомлений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Когда **сетадвисесинк** включает указатель приемника уведомлений формы, храните ссылку на него до тех пор, пока не будет выполнен другой вызов **сетадвисесинк** для отмены уведомления. Отправка уведомления при возникновении изменения в средстве просмотра и при загрузке нового сообщения. 
  
Дополнительную информацию можно узнать в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: Сетадвисесинк  <br/> |MFCMAPI реализует метод **имапивиевконтекст:: сетадвисесинк** в этой функции.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

