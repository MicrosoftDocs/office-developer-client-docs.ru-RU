---
title: IMAPIMessageSiteSubmitMessage
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
  
Запрашивает, чтобы текущее сообщение было в очереди для доставки.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет отправкой сообщения. Можно установить следующий флаг:
    
FORCE_SUBMIT 
  
> MAPI должен отправить сообщение, даже если оно может быть отправлено не сразу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объекты форм вызовите метод **IMAPIMessageSite::SubmitMessage,** чтобы запросить доставку сообщения в очереди. Перед отправкой сообщения сайт сообщения должен вызвать метод [IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md) Сообщение не требуется ранее сохранено, так как **SubmitMessage** должен привести к его сэкономлению, если сообщение было изменено. После возврата **SubmitMessage** форма должна проверить текущее сообщение и затем отклоняться, если нет. 
  
Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI использует метод **IMAPIMessageSite::SubmitMessage** для сохранения сообщения. Сначала вызывается метод **IPersistMessage::HandsOffMessage,** а затем **— SubmitMessage.**  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

