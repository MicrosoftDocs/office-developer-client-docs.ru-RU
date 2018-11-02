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
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576584"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает массив свойств, используемых все формы, установленные в контейнере формы.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как возвращается массив свойства с помощью параметра _ppResults_ . Можно задать следующие флажки: 
    
FORMPROPSET_INTERSECTION 
  
> Возвращаемый массив содержит пересечение свойства форм.
    
FORMPROPSET_UNION 
  
> Возвращаемый массив содержит объединение форм свойства.
    
MAPI_UNICODE 
  
> Строки, возвращаемой в массиве являются в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _ppResults_
  
> [out] Указатель на указатель на структуру возвращенные [SMAPIFormPropArray](smapiformproparray.md) . Эта структура содержит все свойства, используемые с установленным формам. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызовите метод **IMAPIFormContainer::CalcFormPropSet** для получения массива свойства, используемые все формы, установленные в контейнере формы. **IMAPIFormContainer::CalcFormPropSet** работает как метод [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , за исключением того, что он работает в каждую форму, зарегистрированные в конкретным контейнером. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **IMAPIFormContainer::CalcFormPropSet** принимает пересечения или объединение наборов свойств форм, в зависимости от флаг в параметре _ulFlags_ и возвращает структуру **SMAPIFormPropArray** , которая содержит Итоговый группа свойств. 
  
Если клиент передает флаг MAPI_UNICODE _ulFlags_, все возвращенные строки содержат Юникод.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

