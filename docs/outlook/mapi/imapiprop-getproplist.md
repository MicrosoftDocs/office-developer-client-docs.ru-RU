---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414790"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает теги свойств для всех свойств. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битовая метка флагов, которая управляет форматом строк в возвращаемом теге свойства. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lppPropTagArray_
  
> [out] Указатель на указатель на массив тегов свойств, содержащий теги для всех свойств объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Все теги свойств были возвращены успешно.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetPropList** извлекает тег свойства для каждого свойства, поддерживаемого объектом. Если в настоящее время объект не поддерживает какие-либо свойства, **GetPropList** возвращает массив тегов свойств, для члена **cValues** установлено 0. 
  
Область свойств, возвращаемая **GetPropList,** зависит от поставщика. Некоторые поставщики услуг исключают те свойства, к которым у вызываемой связи нет доступа. Все поставщики возвращают свойства **типа** PT_OBJECT.
  
Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже если для объекта не определены свойства строки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики удаленных транспортных услуг **реализуют GetPropList в** точности так, как указано здесь. Особых проблем нет. Конечно, реализация должна возвращать тот же список свойств, что и метод [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить массив тегов свойств, на который указывает _lppPropTagArray._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI использует метод **IMAPIProp::GetPropList** для получения списка свойств, передав его **в GetProps.**  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

