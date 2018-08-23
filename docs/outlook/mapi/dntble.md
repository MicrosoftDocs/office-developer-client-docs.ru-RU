---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565860"
---
# <a name="dntble"></a>DNTBLE

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Информация для загрузки содержимого папки с сервера во время [загрузки состояния в таблице](download-table-state.md). Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
  
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

## <a name="members"></a>Members

 _cEntNew_
  
> [out] Число элементов, добавленных в локальном хранилище. Outlook заполняет это значение во время загрузки при использовании ICS.
    
 _cEntMod_
  
> [out] Число элементов, измененных в локальном хранилище. Outlook заполняет это значение во время загрузки при использовании ICS.
    
 _cEntRead_
  
> [out] Количество элементов чтения или помеченные непрочитанные сообщения для локального хранилища. Outlook заполняет это значение во время загрузки при использовании ICS.
    
 _cEntDel_
  
> [out] Число элементов, удаленных в локальном хранилище. Outlook заполняет это значение во время загрузки при использовании ICS.
    
## <a name="see-also"></a>См. также



[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

