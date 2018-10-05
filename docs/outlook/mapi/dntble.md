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
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391950"
---
# <a name="dntble"></a>DNTBLE

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Информация для загрузки содержимого папки с сервера во время [загрузки состояния в таблице](download-table-state.md). Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.
  
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

