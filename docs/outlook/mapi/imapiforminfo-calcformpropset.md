---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5da9ffdd3021538ec814d1367cf1b06b49cfbc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808907"
---
# <a name="imapiforminfocalcformpropset"></a>IMAPIFormInfo::CalcFormPropSet

  
  
**Относится к**: Outlook 
  
Возвращает указатель на полный набор свойств, используемых в форме.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> В формате Юникод, возвращенных строк. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _ppFormPropArray_
  
> [out] Указатель на указатель на структуру возвращенные [SMAPIFormPropArray](smapiformproparray.md) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |Mfcmapi (en) использует метод **IMAPIFormInfo::CalcFormPropSet** при записи выходных данных отладки для объекты формы.  <br/> |
   
## <a name="see-also"></a>См. также



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

