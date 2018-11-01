---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572307"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запросы, которые сохранены текущего сообщения.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Параметры

Нет.
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
## <a name="remarks"></a>���������

Форм вызовите метод **IMAPIMessageSite::SaveMessage** для запроса сохранить сообщение. 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SaveMessage  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::SaveMessage** для сохранения сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы формы MAPI](mapi-form-interfaces.md)

