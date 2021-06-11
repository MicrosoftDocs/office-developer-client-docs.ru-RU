---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436807"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию для проверки параметров, которые клиентские приложения передали поставщикам услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает путем переумерия метод проверки. 
    
 _First_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Все параметры действительны. 
    
MAPI_E_CALL_FAILED 
  
> Один или несколько параметров не допустимы.
    
## <a name="remarks"></a>Примечания

Параметры, переданные между MAPI и поставщиками услуг, считаются правильными и проходят проверку только отладки с помощью макроса [CheckParms.](checkparms.md) Поставщики должны проверять все параметры, переданные в клиентских приложениях, но клиенты должны предполагать, что параметры MAPI и поставщика являются правильными. Используйте **макрос HR_FAILED** для проверки значений возврата. 
  
 **ПроверкаParms** вызывается по-разному в зависимости от того, является ли код вызова C или C++. C++ передает неявный  параметр, известный как этот, для каждого вызова метода, который становится явным в C и является адресом объекта. Первый параметр  _eMethod_— это код, сделанный из проверяемого интерфейса и метода, и указывает, какие параметры следует найти в стеке. Второй параметр отличается для C и C++. В C++ он называется  _First_ и является первым параметром проверяемого метода. Вторым параметром для языка C,  _ppThis,_ является адрес первого параметра методу, который всегда является указателем объекта. В обоих случаях второй параметр дает адрес начала списка параметров метода и на основе  _eMethod_ перемещается вниз по стеку и проверяет параметры. 
  
Поставщики, реализующие общие интерфейсы, такие как **IMAPITable** и **IMAPIProp,** всегда должны проверять параметры с помощью функции **ValidateParms,** чтобы убедиться в согласованности всех поставщиков. Дополнительные функции проверки параметров были определены для некоторых сложных типов параметров, которые будут использоваться вместо этого по мере необходимости. См. справочные разделы для следующих функций: 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Унаследованные методы используют ту же проверку параметров, что и интерфейс, от которого они наследуют. Например, проверка параметров **для IMessage** и **IMAPIProp** должна быть одинаковой. 
  
## <a name="see-also"></a>См. также



[UlValidateParms](ulvalidateparms.md)

