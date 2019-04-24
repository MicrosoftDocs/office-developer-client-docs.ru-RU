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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299519"
---
# <a name="guid"></a>GUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает глобальный уникальный идентификатор (GUID). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапигуид. h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> Длинное целое значение данных без знака.
    
 **Data2**
  
> Неподписанное короткое целое значение данных.
    
 **Data3**
  
> Неподписанное короткое целое значение данных.
    
 **Data4**
  
> Массив неподписанных символов.
    
## <a name="remarks"></a>Замечания

 Структуры **GUID** используются в MAPI следующим образом: 
  
- В структурах [мапиуид](mapiuid.md) , которые однозначно идентифицируют поставщиков услуг. 
    
- Для идентификаторов интерфейса.
    
- В поле Имя набора свойств именованных свойств. 
    
Поставщики хранилищ сообщений и адресных книг создают структуру **GUID** для использования в структуре **мапиуид** . Передав полученный **мапиуид** в [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md), эти поставщики услуг информируют MAPI об их уникальном идентификаторе.
  
Кроме того, они используются в реализации Microsoft Remote Procedure Call (RPC) и языка описания объектов (ODL). Для получения дополнительных сведений об этих возможностях ознакомьтесь с *руководством программиста по программированИю Microsoft RPC*, справочником по *OLE для программиста* , а также *в OLE*, *втором* выпуске. 
  
Структура **GUID** определена в справочнике *программиста Win32* . Конкретные значения для структур **GUID** , используемых в MAPI, определяются в файле заГоловков MAPI мапигуид. h. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)


[Структуры MAPI](mapi-structures.md)

