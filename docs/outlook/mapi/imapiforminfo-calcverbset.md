---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428783"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель к полному набору глаголов, которые использует форма.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _ppMAPIVerbArray_
  
> [вышел] Указатель на указатель на возвращенную [структуру SMAPIVerbArray,](smapiverbarray.md) которая содержит глаголы формы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Клиентские приложения звонят по методу **IMAPIFormInfo::CalcVerbSet,** чтобы получить указатель на набор глаголов, используемых формой. В **структуре SMAPIVerbArray,** возвращаемой в параметре _ppMAPIVerbArray,_ глаголы возвращаются в порядке номера индекса; Индекс каждого глагола находится в его **члене lVerb.** Клиентские приложения могут использовать массив глаголов для динамической сборки меню, сокрытия или показа кнопок и так далее. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI использует **метод IMAPIFormInfo::CalcVerbSet** при написании вывода отлаговки для информационных объектов форм.  <br/> |
   
## <a name="see-also"></a>См. также



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

