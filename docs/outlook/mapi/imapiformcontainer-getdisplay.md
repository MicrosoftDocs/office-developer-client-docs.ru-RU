---
title: Имапиформконтаинержетдисплай
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329430"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает отображаемое имя контейнера формы.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющая тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Возвращаемая строка имеет формат Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строка имеет формат ANSI.
    
 _Псздисплайнаме_
  
> вышли Указатель на строку, которая содержит отображаемое имя контейнера формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Формконтаинердлг. cpp  <br/> |Кформконтаинердлг:: Кформконтаинердлг  <br/> |MFCMAPI использует метод **имапиформконтаинер::** для получения имени контейнера формы при отображении кформконтаинердлг.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

