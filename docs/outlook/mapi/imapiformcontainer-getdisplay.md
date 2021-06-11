---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416134"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает имя отображения контейнера формы.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенная строка находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, строка находится в формате ANSI.
    
 _pszDisplayName_
  
> [вышел] Указатель на строку с отображаемой именем контейнера формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI использует метод **IMAPIFormContainer::GetDisplay** для получения имени контейнера формы при отрисовке CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

