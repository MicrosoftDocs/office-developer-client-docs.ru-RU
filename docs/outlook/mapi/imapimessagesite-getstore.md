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
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808973"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Относится к**: Outlook 
  
Если такие хранилища возвращает хранилище сообщение, содержащее текущее сообщение. Этот метод возвращает значение NULL в параметре _ppStore_ для внедренных сообщений, которые хранятся в другое сообщение, а не непосредственно в хранилище сообщений. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Параметры

 _ppStore_
  
> [out] Указатель на указатель на хранилище сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Нет без хранилища, содержащий сообщение.
    
## <a name="remarks"></a>Замечания

Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::GetStore** для получения указатель в настоящее время кэширования для заданного хранилища, если она доступна.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

