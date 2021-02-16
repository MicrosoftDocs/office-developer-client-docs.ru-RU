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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает массив свойств, которые использует группа форм.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Параметры

 _pfrminfoarray_
  
> [in] Указатель на массив информационных объектов формы, которые определяют формы, для которых возвращаются свойства.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет возвратом массива свойств в _параметре ppResults._ Можно установить следующие флаги: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращенный массив содержит пересечение свойств формы.
    
FORMPROPSET_UNION 
  
> Возвращенный массив содержит объединение свойств формы.
    
MAPI_UNICODE 
  
> Строки, возвращенные в массиве, имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _ppResults_
  
> [out] Указатель на указатель на возвращенную структуру [SMAPIFormPropArray,](smapiformproparray.md) которая содержит свойства, которые используются формами. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Посетители форм вызывают метод **IMAPIFormMgr::CalcFormPropSet,** чтобы получить массив свойств, которые использует группа форм. **CalcFormPropSet** принимает пересечение или объединение наборов свойств этих форм в зависимости от флага, установленного в параметре  _ulFlags,_ и возвращает структуру **SMAPIFormPropArray,** которая содержит итоговую группу свойств. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки должны быть возвращены в виде строк Юникода. Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается. 
  
## <a name="see-also"></a>См. также



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

