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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347840"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает значение одного свойства из интерфейса свойства, то есть интерфейс, производный от [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Параметры

 _ПМП_
  
> возврата Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , из которого извлекается значение свойства. 
    
 _Улпроптаг_
  
> возврата Тег свойства для извлекаемого свойства. 
    
 _пппроп_
  
> вышли Указатель на указатель на возвращенную структуру [спропвалуе](spropvalue.md) , определяющую полученное значение свойства. 
    
## <a name="return-value"></a>Возвращаемое значение

МАПИ_Е_НОТ_ФАУНД 
  
> Запрошенное свойство недоступно для указанного интерфейса.
    
## <a name="remarks"></a>Примечания

В отличие от метода [IMAPIProp::](imapiprop-getprops.md) /Props, функция **хржетонепроп** никогда не возвращает какое бы то ни было предупреждение. Так как извлекает только одно свойство, оно просто завершается или завершается с ошибкой. Для получения нескольких свойств выполняется быстрее **** . 
  
Вы можете задать или изменить одно свойство с помощью функции [хрсетонепроп](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапифунктионс. cpp  <br/> |Жетмапиобжекттипе  <br/> |MFCMAPI использует метод **хржетонепроп** для получения типа объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

