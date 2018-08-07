---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808979"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**Относится к**: Outlook 
  
Возвращает интерфейс диспетчера формы, который сервера форм можно использовать для открытия другой сервер формы.
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a>Параметры

 _ppFormMgr_
  
> [out] Указатель на указатель на интерфейс диспетчера возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFormManager  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::GetFormManager** для вызова [MAPIOpenFormMgr](mapiopenformmgr.md) и возвращать результаты этого вызова.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIOpenFormMgr](mapiopenformmgr.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

