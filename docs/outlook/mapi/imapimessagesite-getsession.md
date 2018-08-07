---
title: IMAPIMessageSiteGetSession
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
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808975"
---
# <a name="imapimessagesitegetsession"></a>IMAPIMessageSite::GetSession

  
  
**Относится к**: Outlook 
  
Возвращает сеанса MAPI, в которой была создана или открыта текущего сообщения.
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a>Параметры

 _ppSession_
  
> [out] Указатель на указатель на объект возвращенные сеанса.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Не существуют сеансы для текущего сообщения.
    
## <a name="remarks"></a>Замечания

Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::GetSession** возвращает указатель в настоящее время кэширования сеанса, если она доступна.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

