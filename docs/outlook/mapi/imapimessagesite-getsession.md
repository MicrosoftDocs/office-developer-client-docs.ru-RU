---
title: Имапимессажеситежетсессион
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321443"
---
# <a name="imapimessagesitegetsession"></a>IMAPIMessageSite::GetSession

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a>Параметры

 _Ппсессион_
  
> вышли Указатель на указатель на возвращенный объект Session.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Для текущего сообщения не существует сеансов.
    
## <a name="remarks"></a>Замечания

Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: @ Session  <br/> |MFCMAPI использует метод **имапимессажесите::-Session** для возврата текущего кэшированного указателя сеанса, если он доступен.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

