---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808956"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Относится к**: Outlook 
  
Возвращает папку, в которой была создана или открыта, текущего сообщения, если такая папка существует. Этот метод возвращает значение NULL в параметре _ppFolder_ для внедренных сообщений, которые не хранятся непосредственно в папке. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Параметры

 _ppFolder_
  
> [out] Указатель на указатель на папку возвращенные.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Папка не существует в сообщении.
    
## <a name="remarks"></a>Замечания

Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFolder  <br/> |Mfcmapi (en) метод **IMAPIMessageSite::GetFolder** возвращает указатель в настоящее время кэширования данных в указанную папку.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

