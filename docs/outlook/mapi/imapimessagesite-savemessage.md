---
title: Имапимессажеситесавемессаже
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
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321422"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ЗаПрашивает сохранение текущего сообщения.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Параметры

Нет.
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
## <a name="remarks"></a>Замечания

Формы вызывают метод **имапимессажесите:: савемессаже** , чтобы запросить сохранение сообщения. 
  
Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: Савемессаже  <br/> |MFCMAPI использует метод **имапимессажесите:: савемессаже** для сохранения сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

