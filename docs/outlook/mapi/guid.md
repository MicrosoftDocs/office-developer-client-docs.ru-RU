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
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808555"
---
# <a name="guid"></a>GUID

  
  
**Относится к**: Outlook 
  
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

## <a name="members"></a>Members

 **Бд1**
  
> Длинное целое значение данных.
    
 **Бд2**
  
> Целое число без знака короткий данных.
    
 **Data3**
  
> Целое число без знака короткий данных.
    
 **Data4 при**
  
> Массив неподписанных символов.
    
## <a name="remarks"></a>Замечания

 **Идентификатор GUID** структуры используются в MAPI следующим образом: 
  
- В структуре [MAPIUID](mapiuid.md) , которые однозначно идентифицируют поставщиков услуг. 
    
- Для идентификаторов интерфейса.
    
- В свойстве задайте имена именованных свойств. 
    
Хранение сообщений и адресной книги поставщиков создания структуры **идентификатор GUID** для использования в их **MAPIUID** структуры. Путем передачи итоговый **MAPIUID** [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), поставщики услуг Проинформируйте MAPI их уникальный идентификатор.
  
Кроме того они используются в реализации Microsoft удаленного вызова процедур (RPC) и язык описания объектов (ODL). Дополнительные сведения об этих использует иллюстрация *Руководство программиста Microsoft RPC и ссылка*, *OLE Справочник программиста* и *Внутри OLE*, *Второе издание* . 
  
Структура **GUID** определяется в *Справочник программиста Win32* . Определенные значения **GUID** структуры, используемые в рамках MAPI определяются в файле заголовка MAPI Mapiguid.h. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)


[Структуры MAPI](mapi-structures.md)

