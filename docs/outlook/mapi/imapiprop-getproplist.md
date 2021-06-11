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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает теги свойств для всех свойств. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Немного флагов, которые контролируют формат строк в возвращенных тегах свойств. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _lppPropTagArray_
  
> [вышел] Указатель на указатель на массив тегов свойств, содержащий теги для всех свойств объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Все теги свойств были возвращены успешно.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetPropList** извлекает тег свойства для каждого свойства, поддерживаемого объектом. Если объект в настоящее время не поддерживает свойства, **GetPropList** возвращает массив тегов свойств с набором **участника cValues** до 0. 
  
Область свойств, возвращаемая **GetPropList,** варьируется от поставщика к поставщику. Некоторые поставщики услуг исключают те свойства, к которым у вызываемой не имеется доступа. Все поставщики возвращают свойства типа **PT_OBJECT.**
  
Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже если для объекта не определены свойства строки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики удаленных транспортных средств **реализуют GetPropList** точно так, как указано здесь. Особых проблем нет. Конечно, реализация должна возвращать тот же список свойств, который поддерживается методом [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов [функции MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить массив тегов свойств, на который указывает _lppPropTagArray._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI использует **метод IMAPIProp::GetPropList,** чтобы получить список свойств, который будет передан **GetProps.**  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

