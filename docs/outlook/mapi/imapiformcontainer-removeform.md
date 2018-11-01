---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1a1d11db538d9b5368d80962e44b9eab38b490d2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575653"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаление определенной формы из контейнера формы.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Параметры

 _szMessageClass_
  
> [in] Строка, имена класса сообщений для формы для удаления из контейнера формы. Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданной в параметре _szMessageClass_ не соответствует класса сообщений для любой формы в контейнере формы. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) использует метод **IMAPIFormContainer::RemoveForm** для удаления формы из контейнера формы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

