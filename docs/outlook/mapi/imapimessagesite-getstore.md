---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410471"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает хранилище сообщений, которое содержит текущее сообщение, если такое хранилище существует. Этот метод возвращает NULL в  _параметре ppStore_ для внедренных сообщений, которые хранятся в другом сообщении, а не непосредственно в хранилище сообщений. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Параметры

 _ppStore_
  
> [out] Указатель на указатель на хранилище сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Хранилище, в которое входит сообщение, не существует.
    
## <a name="remarks"></a>Примечания

Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI использует метод **IMAPIMessageSite::GetStore** для получения кэшного указателя на указанное хранилище, если оно доступно.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

