---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589175"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает значение одного свойства из интерфейса свойства, то есть интерфейса, полученного из [IMAPIProp.](imapipropiunknown.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameters

 _pmp_
  
> [in] Указатель на [интерфейс IMAPIProp,](imapipropiunknown.md) из которого должно быть извлечено значение свойства. 
    
 _ulPropTag_
  
> [in] Тег свойства извлекаемого свойства. 
    
 _ppprop_
  
> [вышел] Указатель на указатель на возвращенную [структуру SPropValue,](spropvalue.md) определяющий извлеченное значение свойства. 
    
## <a name="return-value"></a>Возвращаемое значение

MAPI_E_NOT_FOUND 
  
> Запрашиваемая свойство недоступна из указанного интерфейса.
    
## <a name="remarks"></a>Примечания

В отличие [от метода IMAPIProp::GetProps,](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает никаких предупреждений. Так как оно извлекает только одно свойство, оно просто успешно или не удается. Для получения нескольких свойств **GetProps быстрее.** 
  
Можно установить или изменить одно свойство с помощью [функции HrSetOneProp.](hrsetoneprop.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI использует метод **HrGetOneProp** для получения типа объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

