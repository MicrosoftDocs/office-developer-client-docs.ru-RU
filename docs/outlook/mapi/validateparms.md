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
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579720"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает перечисление, метод для проверки. 
    
 _Первый_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Все параметры являются допустимыми. 
    
MAPI_E_CALL_FAILED 
  
> Один или несколько параметров являются недопустимыми.
    
## <a name="remarks"></a>Замечания

Параметры, переданные между MAPI и службой поставщиков предполагается, что правильно и подвергаются только проверки отладка с помощью макроса [CheckParms](checkparms.md) . Поставщики должен проверить, все параметры, переданные в клиентских приложениях, но клиенты должны предполагается правильность параметров и MAPI. Использование макроса **HR_FAILED** для проверки возвращаемого значения. 
  
 **ValidateParms** называется по-разному в зависимости от того, является ли вызывающий кода C или C++. C++ передает неявный параметр известных как _это_ для каждого вызова метода, который становится явные в C и представляет собой адрес объекта. Первый параметр _eMethod_является перечислителя из интерфейса и метод проверки и сообщает о том, какие параметры следует ожидать для поиска в стеке. Второй параметр – C и C++ различные. В C++ он вызывает _первый_и является первым параметром в метод при проверке. Второй параметр для языка C, _ppThis_представляет собой адрес первого параметра в метод, который всегда указателя на объект. В обоих случаях второй параметр содержит адрес в начало списка параметров метода и на основе _eMethod_, перемещает вниз стека и проверяет параметры. 
  
Поставщики, реализующие общие интерфейсы, такие как **IMAPITable** и **IMAPIProp** всегда следует выполнять проверку параметров с помощью функции **ValidateParms** , чтобы сделать что согласованность между всех поставщиков. Функции проверки дополнительный параметр были определены для некоторых сложных типов параметров для использования вместо соответствующим образом. Можно найти ссылки на разделы для следующих функций: 
  
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
    
Унаследованные методы используйте одинаковые параметр проверки как интерфейс, от которого они унаследованы. Например проверка параметров для **IMessage** и **IMAPIProp** должно совпадать. 
  
## <a name="see-also"></a>См. также



[UlValidateParms](ulvalidateparms.md)

