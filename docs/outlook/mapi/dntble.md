---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337116"
---
# <a name="dntble"></a>DNTBLE

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Информация для скачивания содержимого папки с сервера при [загрузке таблицы состояние](download-table-state.md). Процесс скачивания использует синхронизацию добавочных изменений (ICS) Microsoft Exchange. Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Элементы

 _cEntNew_
  
> [out] Количество элементов, добавленных в локальное хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
 _cEntMod_
  
> [out] Количество элементов, измененных в локальном хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
 _cEntRead_
  
> [out] Количество элементов, прочитанных или помеченных как непрочитанные в локальном хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
 _cEntDel_
  
> [out] Количество элементов, удаленных из локального хранилища. Outlook заполнит это значение во время скачивания при использовании ICS.
    
## <a name="see-also"></a>См. также



[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

