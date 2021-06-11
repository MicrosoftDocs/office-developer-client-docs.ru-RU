---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436428"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает массив свойств, которые использует группа форм.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameters

 _pfrminfoarray_
  
> [in] Указатель на массив объектов информации о формах, которые определяют формы, для которых нужно возвращать свойства.
    
 _ulFlags_
  
> [in] Битмашка флагов, которая управляет тем, как возвращается массив свойств в параметре _ppResults._ Можно установить следующие флаги: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращенный массив содержит пересечение свойств формы.
    
FORMPROPSET_UNION 
  
> Возвращенный массив содержит объединение свойств формы.
    
MAPI_UNICODE 
  
> Строки, возвращенные в массиве, находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _ppResults_
  
> [вышел] Указатель на указатель на возвращенную [структуру SMAPIFormPropArray,](smapiformproparray.md) которая содержит свойства, которые используются формами. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Зрители форм называют **метод IMAPIFormMgr::CalcFormPropSet** для получения массива свойств, которые использует группа форм. **CalcFormPropSet** принимает пересечение или объединение наборов свойств этих форм в зависимости от флага, заданного в параметре  _ulFlags,_ и возвращает структуру **SMAPIFormPropArray,** содержаную в результате группу свойств. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если зритель формы передает флаг MAPI_UNICODE в параметре  _ulFlags,_ все строки должны быть возвращены в виде строк Юникод. Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена. 
  
## <a name="see-also"></a>См. также



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

