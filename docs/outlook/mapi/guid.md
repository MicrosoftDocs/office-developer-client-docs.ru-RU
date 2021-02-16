---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421587"
---
# <a name="guid"></a>GUID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает глобальный уникальный идентификатор (GUID). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiguid.h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>"Участники"

 **Data1**
  
> Неподписаное длинное значение данных.
    
 **Data2**
  
> Неподписано короткое значение данных.
    
 **Data3**
  
> Неподписано короткое значение данных.
    
 **Data4**
  
> Массив неподписаных символов.
    
## <a name="remarks"></a>Примечания

 **Структуры GUID** используются в MAPI следующим образом: 
  
- В [структурах MAPIUID,](mapiuid.md) которые однозначно определяют поставщиков услуг. 
    
- Для идентификаторов интерфейса.
    
- В наборе свойств имена именуемого свойства. 
    
Поставщики хранения сообщений и адресных книг создают структуру **GUID** для использования в своей структуре **MAPIUID.** Передав итоговые **данные MAPIUID** в [IMAPISupport::SetProviderUID,](imapisupport-setprovideruid.md)эти поставщики услуг сообщают MAPI о своем уникальном идентификаторе.
  
Кроме того, они используются в реализации удаленного вызова процедур (RPC) Майкрософт и языка описания объектов (ODL). Дополнительные сведения об этих вариантах использования см. в руководстве и справочнике по microsoft *RPC Programmer,* справочнике *по OLE Programmer* и *inside OLE*, *Second Edition.* 
  
Структура **GUID** определена в справочнике *win32 Programmer..* Определенные значения для структур **GUID,** используемых в MAPI, определяются в файле загона MAPI Mapiguid.h. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)


[Структуры MAPI](mapi-structures.md)

