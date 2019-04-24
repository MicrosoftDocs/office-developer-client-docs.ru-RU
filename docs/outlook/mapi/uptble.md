---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329710"
---
# <a name="uptble"></a>UPTBLE

**Область применения**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения для отправки содержимого папки во время [состояния таблицы отправки](upload-table-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Элементы

 _Иентмод_
  
>  вышли Индекс для отслеживания отправки _центмод_ числа новых или измененных элементов. 
    
 _cEntMod_
  
>  вышли Количество новых или измененных элементов в папке. 
    
 _Иентреад_
  
>  вышли Индекс для отслеживания отгрузки числа прочитанных элементов _центреад_ . 
    
 _cEntRead_
  
>  вышли Количество прочитанных элементов в папке. 
    
 _Иентдел_
  
>  вышли Индекс для отслеживания отправки числа удаленных элементов _центдел_ . 
    
 _cEntDel_
  
>  вышли Количество удаленных элементов в папке. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

