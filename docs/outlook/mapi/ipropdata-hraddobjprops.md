---
title: ипропдатахраддобжпропс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416386"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет одно или несколько свойств типа PT_OBJECT в объект.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _лппроптагаррай_
  
> возврата Указатель на массив тегов свойств, указывающий свойства, которые требуется добавить.
    
 _лпппроблемс_
  
> [вход, выход] На входе, допустимый указатель на структуру [спроппроблемаррай](spropproblemarray.md) или значение null. В выходных данных указатель на указатель на структуру, содержащую сведения о свойствах, которые не удалось добавить, или значение NULL. Указатель на структуру массива неполадок свойств возвращается только в том случае, если передается допустимый указатель. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно добавлены.
    
MAPI_E_INVALID_TYPE 
  
> В массиве, на который указывает параметр _лппроптагаррай_ , был передан тип свойства, отличный от PT_OBJECT. 
    
MAPI_E_NO_ACCESS 
  
> Для объекта задано разрешение на чтение и запись.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Некоторые (но не все) свойства были добавлены.
    
## <a name="remarks"></a>Примечания

Метод **ипропдата:: храддобжпропс** добавляет одно или несколько свойств типа PT_OBJECT в объект. **Храддобжпропс** предоставляет альтернативу методу [IMAPIProp:: SetProps](imapiprop-setprops.md) для свойств объекта, так как свойства объекта невозможно создать с помощью метода **SetProps**. При добавлении свойства объекта в тег свойства включается в список тегов свойств, возвращаемых методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **храддобжпропс** возвращает MAPI_W_PARTIAL_COMPLETION и вы настроили _лпппроблемс_ на допустимый указатель, Проверьте возвращаемую структуру [спроппроблемаррай](spropproblemarray.md) , чтобы узнать, какие свойства не были добавлены. Как правило, единственная неполадка связана с нехваткой памяти. Освободите структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) по завершении работы с ней. 
  
Для добавления свойства целевой объект должен иметь разрешение на чтение и запись. Если **храддобжпропс** возвращает MAPI_E_NO_ACCESS, невозможно добавить свойства для объекта, так как он не разрешает изменение. Чтобы получить разрешение на чтение и запись объекта перед вызовом **храддобжпропс**, вызовите [Ипропдата:: хрсетобжакцесс](ipropdata-hrsetobjaccess.md) и присвойте параметру _улакцесс_ значение IPROP_READWRITE. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

