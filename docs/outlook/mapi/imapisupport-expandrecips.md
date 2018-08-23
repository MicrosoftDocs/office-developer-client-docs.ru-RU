---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591013"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Завершает список получателей сообщения, возможность расширения списков рассылок определенного.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, содержащее список получателей для обработки.
    
 _lpulFlags_
  
> [out] Указатель на битовую маску флагов, определяющее тип действия, выполняемые. Можно задать следующие флажки:
    
NEEDS_PREPROCESSING 
  
> Должна быть предварительно перед отправкой сообщения.
    
NEEDS_SPOOLER 
  
> Диспетчер очереди MAPI (а не поставщика транспорта, к которому тесно связан вызывающего абонента) необходимо отправить сообщение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Список получателей сообщения успешно обработан.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::ExpandRecips** реализуется для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений вызова **ExpandRecips** запроса MAPI для выполнения следующих задач: 
  
- Разверните узел определенные списки рассылки их компонент получателям.
    
- Замените все отображаемые имена, которые были изменены исходные имена.
    
- Пометьте все дублированные записи.
    
- Устраните все одноразовых адреса. 
    
- Проверьте ли сообщение должно предварительной обработки и если это так, необходимо задать флаг, на который указывает _lpulFlags_ для NEEDS_PREPROCESSING. 
    
 **ExpandRecips** развертывание списков рассылки, обмена мгновенными сообщениями тип адреса MAPIPDL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Всегда вызывайте **ExpandRecips** как часть вашей обработки сообщений. Позвоните **ExpandRecips** один первого вызовов в реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

