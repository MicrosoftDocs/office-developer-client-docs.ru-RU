---
title: Имапиформконтаинерремовеформ
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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432200"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет определенную форму из контейнера формы.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Параметры

 _Сзмессажекласс_
  
> возврата Строка, которая называет класс сообщения формы, удаляемой из контейнера формы. Имена классов сообщений всегда являются строками ANSI, а не Юникодом.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_НОТ_ФАУНД 
  
> Класс сообщения, переданный в параметре _сзмессажекласс_ , не соответствует классу сообщения любой формы в контейнере формы. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Формконтаинердлг. cpp  <br/> |Кформконтаинердлг:: Онделетеселектедитем  <br/> |MFCMAPI использует метод **имапиформконтаинер:: ремовеформ** для удаления формы из контейнера формы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

