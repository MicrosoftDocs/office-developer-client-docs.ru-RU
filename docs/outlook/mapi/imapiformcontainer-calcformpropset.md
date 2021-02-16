---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414916"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает массив свойств, используемых всеми формами, установленными в контейнере формы.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет возвратом массива свойств в параметре _ppResults._ Можно установить следующие флаги: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращенный массив содержит пересечение свойств форм.
    
FORMPROPSET_UNION 
  
> Возвращенный массив содержит объединение свойств форм.
    
MAPI_UNICODE 
  
> Строки, возвращенные в массиве, имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _ppResults_
  
> [out] Указатель на указатель на возвращенную [структуру SMAPIFormPropArray.](smapiformproparray.md) Эта структура содержит все свойства, используемые установленными формами. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывают метод **IMAPIFormContainer::CalcFormPropSet,** чтобы получить массив свойств, используемых всеми формами, установленными в контейнере формы. **IMAPIFormContainer::CalcFormPropSet** работает как метод [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) за исключением того, что он работает в каждой форме, зарегистрированной в конкретном контейнере. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **IMAPIFormContainer::CalcFormPropSet** принимает пересечение или объединение наборов свойств форм в зависимости от флага, установленного в параметре  _ulFlags,_ и возвращает структуру **SMAPIFormPropArray,** которая содержит итоговую группу свойств. 
  
Если клиент передает флаг MAPI_UNICODE в  _ulFlags,_ все возвращенные строки будут Юникод.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

