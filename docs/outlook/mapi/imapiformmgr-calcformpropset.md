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
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808916"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Относится к**: Outlook 
  
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
  
> [in] Указатель на массив объектов данные формы, чтобы указать форм, для которого возвращаются свойства.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как возвращается массив свойства с помощью параметра _ppResults_ . Можно задать следующие флажки: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращаемый массив содержит пересечение свойств формы.
    
FORMPROPSET_UNION 
  
> Возвращаемый массив содержит объединение свойств формы.
    
MAPI_UNICODE 
  
> Строки, возвращаемой в массиве являются в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _ppResults_
  
> [out] Указатель на указатель на возвращенный [SMAPIFormPropArray](smapiformproparray.md) структуру, которая содержит свойства, используйте формы. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызвать метод **IMAPIFormMgr::CalcFormPropSet** для получения массива свойств, которые использует группа форм. **CalcFormPropSet** принимает либо пересечения или объединение эти формы свойство задает, в зависимости от флаг в параметр _ulFlags_ и возвращает структуру **SMAPIFormPropArray** , содержащий итоговый группу свойства. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки должны возвращаться Юникод. Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE. 
  
## <a name="see-also"></a>См. также



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

