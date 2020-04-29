---
title: имапимессажеситесубмитмессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417030"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запрашивает доставку текущего сообщения в очередь на доставку.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ отправки сообщения. Можно задать следующий флаг:
    
FORCE_SUBMIT 
  
> MAPI должен отправить сообщение, даже если оно не может быть отправлено немедленно.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объекты формы вызывают метод **имапимессажесите:: субмитмессаже** , чтобы запросить доставку сообщения в очередь на доставку. Сайт сообщения должен вызвать метод [иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) перед отправкой сообщения. Сообщение не обязательно было сохранено ранее, так как **субмитмессаже** должно привести к сохранению сообщения, если оно было изменено. После возврата **субмитмессаже**форма должна проверять текущее сообщение, а затем отклонить его, если он не существует. 
  
Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: Субмитмессаже  <br/> |MFCMAPI использует метод **имапимессажесите:: субмитмессаже** для сохранения сообщения. Сначала он вызывает метод **иперсистмессаже:: хандсоффмессаже** , а затем вызывает **субмитмессаже**.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

