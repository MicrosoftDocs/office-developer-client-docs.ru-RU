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
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808692"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Относится к**: Outlook 
  
Извлекает значения одного свойства из интерфейса свойство, то есть, производные от [IMAPIProp](imapipropiunknown.md)интерфейс. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Параметры

 _pmp_
  
> [in] Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , из которого выполняется получение значения свойства. 
    
 _ulPropTag_
  
> [in] Свойство tag свойства нужно вернуть. 
    
 _ppprop_
  
> [out] Указатель на указатель на структуру возвращенные [SPropValue](spropvalue.md) , определяющий значение извлеченное свойство. 
    
## <a name="return-value"></a>������������ ��������

MAPI_E_NOT_FOUND 
  
> Свойство недоступен из указанного интерфейса.
    
## <a name="remarks"></a>Замечания

В отличие от метода [IMAPIProp::GetProps](imapiprop-getprops.md) функция **HrGetOneProp** никогда не возвращает все предупреждения. Так как он получает только одно свойство, он просто либо успешного или неудачного завершения. Для получения значений нескольких свойств, **GetProps** выполняется быстрее. 
  
Можно установить или изменить отдельное свойство с помощью функции [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |Mfcmapi (en) используется метод **HrGetOneProp** для получения типа объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

