---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582562"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель интерфейса библиотеку локального формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>Параметры

 _ppfcnt_
  
> [out] Указатель на указатель на интерфейс библиотеки локального формы.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Интерфейс, для которого возвращается указатель можно использовать с помощью программ сторонних производителей установки для установки отдельных приложений форм в библиотеку без программа предварительного войдите в систему MAPI. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnMAPIOpenLocalFormContainer  <br/> |Mfcmapi (en) использует метод **MAPIOpenLocalFormContainer** для открытия контейнера локального формы для отображения в новом окне.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

